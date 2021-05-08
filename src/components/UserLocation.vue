<template>
  <h2 class="title-block" v-if="sumbitted == false">
    GET YOUR Tradenet Simulator Now!
  </h2>
  <transition name="slide-fade" mode="out-in">
    <div class="form-container" v-if="sumbitted == false" key="slide1">
      <h3 class="form-title">
        Make sure your details <span>are entered accurately </span>Tradenet will
        reject any
        <span>incorrectly filled applications</span>
      </h3>
      <small v-if="errors.name">{{ errors.name }}</small>
      <small v-if="errors.email">{{ errors.email }}</small>
      <small v-if="errors.address">{{ errors.address }}</small>
      <form
        class="form"
        @submit.prevent="submitHandler"
        v-if="sumbitted == false"
      >
        <div class="input-wrapper">
          <input
            type="text"
            placeholder="Name"
            class="input"
            v-model.trim="form.name"
          />
          <input
            type="email"
            placeholder="Email"
            class="input"
            v-model.trim="form.email"
          />
          <select v-model="form.address" class="input">
            <option value="" disabled selected hidden>Country</option>
            <option
              v-for="country in countries"
              :value="country.value"
              :key="country"
            >
              {{ country.label }}
            </option>
          </select>

          <vue-tel-input
            v-model="form.phone"
            mode="international"
            class="input"
          ></vue-tel-input>
        </div>
        <div class="checkbox-container">
          <input type="checkbox" class="checkbox" v-model="form.agreeded" />
          <p class="agree-policy">
            I consent to receive promotional materials from time to time. I,
            hereby declare that I have read, understood and accepted the
            <a href="#"
              >Company‘s Terms Conditions | Privacy policy and cookie policy</a
            >
          </p>
        </div>
        <button class="btn btn-lg">GET NOW</button>
      </form>
    </div>

    <div class="slide2" v-else key="slide2">
      <div class="wrapper-block">
        <h3 class="title">That’s it!</h3>
        <h5 class="subtitle">
          Thank you for choosing us! Check our resources and dive in the world
          of day trading now!
        </h5>
        <div class="block-image">
          <div class="image-item-1">
            <h2 class="title">Free Сourse</h2>
            <h5 class="subtitle">
              Take our free course
              <span>and start your day trading journey today!</span>
            </h5>
          </div>
          <div class="image-item-2">
            <h2 class="title">Trading challenge</h2>
            <h5 class="subtitle">
              Take the 5-day challenge <span>and win amazing prizes</span>
            </h5>
            <div class="fb-wrapper">
              <img
                src="../assets/Facebook_icon-mobile.png"
                alt="Facebook_icon-mobile"
                class="fb-logo-mobile"
                width="45"
                height="44"
              />
            </div>
          </div>
          <div class="image-item-3">
            <h2 class="title">Tradenet Stock Talks</h2>
            <img
              src="../assets/facebook-logo.png"
              alt="facebook-logo"
              class="logo"
              width="60"
              height="59"
            />
            <h5 class="subtitle">
              Join our Facebook community of successful traders and learn from
              the best
            </h5>
            <img
              src="../assets/slide3-dop.png"
              alt="slide3"
              class="laptop"
              width="244"
              height="166"
            />
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
import axios from "axios";

import { VueTelInput } from "vue3-tel-input";
import "vue3-tel-input/dist/vue3-tel-input.css";

const countries = require("i18n-iso-countries");
countries.registerLocale(require("i18n-iso-countries/langs/en.json"));

export default {
  data() {
    return {
      form: {
        name: "",
        address: "",
        email: "",
        phone: "",
        agreeded: false,
      },
      errors: {
        name: null,
        email: null,
        country: null,
      },
      sumbitted: false,
      options: [],
    };
  },
  components: {
    VueTelInput,
  },
  computed: {
    countries() {
      const list = countries.getNames("en", { select: "official" });
      return Object.keys(list).map((key) => ({ value: key, label: list[key] }));
    },
  },
  mounted() {
    this.locator();
  },
  methods: {
    locator() {
      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(
          (position) => {
            this.getAddressFrom(
              position.coords.latitude,
              position.coords.longitude
            );
          },
          (error) => {
            console.log(error.message);
          }
        );
      } else {
        this.from.address = response.data.results[0].formatted_address;
      }
    },
    getAddressFrom(lat, long) {
      axios
        .get(
          "https://maps.googleapis.com/maps/api/geocode/json?latlng=" +
            lat +
            "," +
            long +
            "&key=yourApiKey"
        )
        .then((response) => {
          if (response.data.error_message) {
            console.log(response.data.error_message);
          } else {
            console.log(response.data.results[0].formatted_address);
          }
        })
        .catch((error) => {
          console.log(error.message);
        });
    },
    formIsValid() {
      let isValid = true;

      if (this.form.name.length <= 3) {
        this.errors.name = "Имя не может быть меньше 3";
        isValid = false;
        this.sumbitted = false;
      } else {
        this.errors.name = null;
      }
      if (this.form.email.length === 0) {
        this.errors.email = "email не может быть пустым";
        isValid = false;
        this.sumbitted = false;
      } else {
        this.errors.email = null;
      }
      if (this.form.address.length === 0) {
        this.errors.address = "Country не может быть пустым";
        isValid = false;
        this.sumbitted = false;
      } else {
        this.errors.address = null;
      }

      return isValid;
    },
    submitHandler() {
      if (this.formIsValid()) {
        console.log("Data:", this.form);
        this.sumbitted = true;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
// animation form
.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateX(10px);
  opacity: 0;
}

.title-block {
  color: #fff;
  font-weight: bold;
  font-size: 24px;
  line-height: 28px;
  text-transform: uppercase;
  margin: 0 auto 40px auto;
  width: 324px;
  text-align: center;
}
.form-container {
  background: #ffffff;
  box-shadow: 4px 4px 40px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
  width: 673px;
  padding: 15px 25px;
  margin: 0 auto;
  .form-title {
    font-weight: 500;
    font-size: 16px;
    line-height: 19px;
    text-align: center;
    color: #f80303;
    max-width: 406px;
    margin: 0 auto 0 auto;
  }
  small {
    display: block;
    color: darkred;
    text-align: center;
    margin-top: 5px;
    margin-bottom: 5px;
  }
  .form {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    .input-wrapper {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      height: 180px;
      align-items: center;
      justify-content: center;
    }
    .input {
      border: 1px solid #dadada;
      box-sizing: border-box;
      border-radius: 10px;
      width: 300px;
      height: 38px;
      margin-right: 10px;
      margin-top: 25px;
      outline: none;
      padding-left: 10px;
    }
    .checkbox-container {
      display: flex;
      margin-top: 20px;
      margin-bottom: 20px;
      margin-left: 8px;
      max-width: 583px;
      .checkbox {
        border: 1px solid #ababab;
        box-sizing: border-box;
        border-radius: 5px;
        width: 32px;
        height: 20px;
        margin-right: 20px;
      }
      .agree-policy {
        color: #ababab;
        font-weight: 300;
        font-size: 10px;
        line-height: 12px;
        letter-spacing: 0.05em;
        a {
          color: black;
          text-decoration: none;
        }
      }
    }
    .btn-lg {
      margin: 0 auto;
    }
  }
}
.slide2 {
  background: #ffffff;
  box-shadow: 0px 4px 90px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
  width: 996px;
  margin: 0 auto;
  .wrapper-block {
    text-align: center;
    padding-top: 60px;
    padding-bottom: 60px;
    .title {
      font-weight: 500;
      font-size: 32px;
      line-height: 38px;
      padding-bottom: 20px;
    }
    .subtitle {
      font-weight: normal;
      font-size: 24px;
      line-height: 28px;
      margin: 0 auto 40px auto;
      max-width: 540px;
    }
    .block-image {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
      color: #fff;
      .image-item-1 {
        background: url("../assets/slide1.jpg") 100% 100%;
        background-repeat: no-repeat;
        background-size: cover;
        border-radius: 5px;
        margin-right: 60px;
        padding: 35px 13px 0;
        text-align: left;
        width: 263px;
        height: 386px;
      }
      .image-item-2 {
        background: url("../assets/slide2.jpg") 100% 100%;
        background-repeat: no-repeat;
        background-size: cover;
        border-radius: 5px;
        margin-right: 60px;
        padding: 35px 13px 0;
        text-align: left;
        background-position: center;
        width: 263px;
        height: 386px;
        .fb-logo-mobile {
          display: none;
        }
      }
      .image-item-3 {
        background: url("../assets/slide3.jpg") 100% 100%;
        background-repeat: no-repeat;
        background-size: cover;
        border-radius: 5px;
        padding: 35px 13px 0;
        text-align: left;
        position: relative;
        width: 263px;
        height: 386px;
        .logo {
          position: absolute;
          right: 6px;
          top: 10px;
        }
        .laptop {
          position: relative;
          bottom: 181px;
        }
      }
      .title {
        font-weight: bold;
        font-size: 30px;
        line-height: 36px;
        max-width: 183px;
      }
      .subtitle {
        font-size: 16px;
        line-height: 19px;
        max-width: 229px;
        padding-bottom: 162px;
        span {
          display: block;
        }
      }
    }
  }
}
@media (max-width: 320px) {
  .form-container {
    width: 290px !important;
    padding: 20px !important;
    .form-title {
      max-width: 220px !important;
      text-transform: uppercase;
      font-size: 12px;
      line-height: 14px;
      span {
        display: block;
      }
    }
    .btn-lg {
      width: 250px;
      height: 42px;
      padding: 0;
      font-size: 16px;
    }
    .form {
      .input-wrapper {
        flex-direction: initial;
        height: 100%;
      }
      .input {
        width: 250px;
      }
      .checkbox {
        width: 20% !important;
        height: 30% !important;
        margin-right: 12px !important;
      }
    }
  }
  .slide2 {
    width: 290px;
    height: 551px;
    .wrapper-block {
      padding: 20px 25px 20px 20px;
      text-align: left;
      .title {
        font-size: 20px;
        line-height: 24px;
        padding-bottom: 10px;
      }
      .subtitle {
        font-size: 16px;
        line-height: 19px;
        max-width: 235px;
        margin: 0 auto 20px auto !important;
      }
      .block-image {
        height: 100%;
        .image-item-1 {
          background: url("../assets/slide1-mobile.png") no-repeat 100% 100%;
          background-size: cover;
          margin: 0;
          padding: 20px 20px 20px 25px;
          margin-bottom: 10px;
          width: 250px;
          height: 120px;
        }
        .image-item-2 {
          background: url("../assets/slide2-mobile.png") no-repeat 100% 100%;
          background-size: cover;
          margin: 0;
          padding: 20px 20px 20px 25px;
          margin-bottom: 10px;
          width: 250px;
          height: 120px;
          .fb-wrapper {
            display: flex !important;
            justify-content: flex-end !important;
            position: relative !important;
            bottom: 50px !important;
            left: 10px !important;
          }
          .fb-logo-mobile {
            display: block !important;
          }
        }
        .image-item-3 {
          background: url("../assets/slide3-mobile.png") no-repeat 100% 100%;
          background-size: cover;
          margin: 0;
          padding: 20px 20px 20px 25px;
          width: 250px;
          height: 120px;
          .logo {
            display: none;
          }
          .laptop {
            display: none;
          }
        }
        .title {
          font-size: 20px;
          line-height: 24px;
          max-width: 100%;
        }
        .subtitle {
          padding-bottom: 0;
          max-width: 100%;
          margin: 0;
          font-size: 14px;
          line-height: 17px;
        }
      }
    }
  }
}
</style>