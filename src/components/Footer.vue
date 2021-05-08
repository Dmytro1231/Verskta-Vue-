<template>
  <div class="container">
    <div class="wrapper">
      <div class="about-us">
        <div class="block-info">
          <h4 class="title">Education</h4>
          <p><a href="#">Self-study course</a></p>
          <p><a href="#">Star trader course</a></p>
          <p><a href="#">Top trader course</a></p>
          <p><a href="#">Mentorship Program</a></p>
          <p><a href="#">Global markets course</a></p>
        </div>
        <div class="block-info">
          <h4 class="title">About</h4>
          <p><a href="#">About us</a></p>
          <p><a href="#">About Meir Barak</a></p>
          <p><a href="#">Meet Our Team</a></p>
          <p><a href="#">Refer A Friend</a></p>
          <p><a href="#">Contact Us</a></p>
        </div>
        <div class="block-info">
          <h4 class="title">Our Programs</h4>
          <p><a href="#">Intro Package</a></p>
          <p><a href="#">Student Package</a></p>
          <p><a href="#">Expert Package</a></p>
          <p><a href="#">Pro Package</a></p>
        </div>
        <div class="block-info">
          <h4 class="title">Usefull links</h4>
          <div class="icon">
            <img
              src="../assets/Vector1.png"
              alt="Vector1"
              width="16"
              height="16"
            />
            <p><a href="#">Challenge</a></p>
          </div>
          <div class="icon">
            <img
              src="../assets/Vector2.png"
              alt="Vector2"
              width="16"
              height="12"
            />
            <p><a href="#">Start Learning</a></p>
          </div>
          <div class="icon">
            <img
              src="../assets/Vector3.png"
              alt="Vector3"
              width="16"
              height="12"
            />
            <p><a href="#">Newsletter</a></p>
          </div>
          <div class="icon">
            <img
              src="../assets/Vector4.png"
              alt="Vector4"
              width="12"
              height="8"
            />
            <p><a href="#">Class Schedule</a></p>
          </div>
        </div>
        <div class="block-info">
          <h4 class="title">Contacts</h4>
          <p><a href="mailto:info@tradenet.com">info@tradenet.com</a></p>
          <a href="tel:+1-516-210-4148">+1-516-210-4148</a>
          <p>Tradenet Capital Markets Ltd.</p>
        </div>
        <div class="social">
          <a href="#">
            <img
              src="../assets/youtube.png"
              alt="youtube"
              width="19"
              height="15"
            />
            <small class="hidden">Our YouTube</small></a
          >

          <a href="#">
            <img
              src="../assets/facebook.png"
              alt="facebook"
              width="12"
              height="19"
            />
            <small class="hidden">Our Facebook</small></a
          >
          <a href="#"
            ><img
              src="../assets/instagram.png"
              alt="instagram"
              width="18"
              height="17"
            />
            <small class="hidden">Our Instagram</small>
          </a>
          <a href="#">
            <img
              src="../assets/twitter.png"
              alt="twitter"
              width="19"
              height="17"
            />
            <small class="hidden">Our Twitter</small>
          </a>
        </div>
      </div>
      <div class="payment">
        <img
          src="../assets/payment.png"
          alt="payment"
          width="390"
          height="34"
        />
      </div>
      <hr class="footer-line" />
      <div class="block-text">
        <p class="slogan">
          Tradenet is a day trading training school. We offer courses including
          stock trading, CFDs, options, futures and foreign exchange. At
          Tradenet, we specialize in providing day trading courses with
          inexperienced beginners and experienced traders. We offer three
          learning options: self-taught online courses, so you can study at home
          network teaching there is a unique one-on-one teaching. We also offer
          online real-time discussion groups. Most of our services have several
          language options, including Spanish, German, French, Russian,
          Hungarian, Italian, Arabic, etc.<span>
            * Tradenet only provides educational services and will not be held
            liable for any disputes regarding the private investment firms.
            student acceptance to provide trading services remains at the sole
            discretion of the private investment firms. Buying a Tradenet
            education package does not guarantee access to a funded account.
            Tradenet provides a 14-day money back guarantee policy for students
            that were not accepted to trade a private investment firm funded
            account.</span
          >
        </p>
      </div>
      <div class="footer-logo">
        <a href="#">
          <img src="../assets/logow.png" alt="logow" width="94" height="30" />
        </a>
        <div class="policy">
          <p><a href="#">Terms of Use</a></p>
          <p><a href="#">Privacy Policy</a></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  background: #394046;
  .wrapper {
    max-width: 1110px;
    margin: 0 auto;
    padding-top: 65px;
    .about-us {
      display: flex;
      flex-direction: row;
      color: #fff;
      .block-info {
        margin-right: 59px;
        max-width: 170px;
        .title {
          font-size: 20px;
          line-height: 24px;
          margin-bottom: 11px;
        }
        a {
          text-decoration: none;
          color: #fff;
          margin-bottom: 6px;
        }
        p {
          font-size: 14px;
          line-height: 17px;
          &:not(:last-child) {
            margin-bottom: 6px;
          }
          &:last-child {
            margin-top: 6px;
          }
        }
        .icon {
          display: flex;
          align-items: baseline;
          img {
            margin-right: 7px;
          }
        }
      }
      .social {
        margin-left: 13px;
        a:not(:last-child) {
          margin-right: 22px;
        }
        a .hidden {
          display: none;
        }
      }
    }
    .payment {
      display: flex;
      justify-content: flex-end;
      margin-top: 21px;
      margin-bottom: 26px;
    }
    .block-text {
      margin-top: 48px;
      color: #fff;
      .slogan {
        font-size: 16px;
        line-height: 155%;
        letter-spacing: 0.37px;
        span {
          display: block;
          margin-top: 40px;
          margin-bottom: 48px;
        }
      }
    }
    .footer-logo {
      display: flex;
      justify-content: space-between;
      padding-bottom: 64px;
      .policy {
        color: #fff;
        display: flex;
        a {
          margin-right: 22px;
          text-decoration: none;
          color: #fff;
          font-size: 14px;
          line-height: 17px;
        }
      }
    }
  }
}
@media (max-width: 320px) {
  .wrapper {
    padding-top: 40px !important;
    margin: 0 35px 0 35px !important;
    width: 100% !important;
    .about-us {
      flex-wrap: wrap;
      .block-info {
        margin-right: 40px !important;
        margin-bottom: 40px !important;
        .title {
          font-size: 16px !important;
          line-height: 19px !important;
        }
        p {
          font-size: 10px !important;
          line-height: 12px !important;
          max-width: 100px !important;
        }
        a {
          font-size: 10px;
          line-height: 12px;
        }
      }
      .social {
        display: grid;
        margin-left: 0 !important;
        align-items: baseline !important;
        grid-template-rows: 25px 30px 28px 20px;
        a {
          text-decoration: none;
          color: #fff;
          display: flex;
          align-items: center;
          margin-right: 0 !important;
          small {
            font-weight: 500;
            font-size: 10px;
            line-height: 12px;
            margin-left: 9px;
          }
          .hidden {
            display: block !important;
          }
        }
      }
    }
    .payment {
      display: none !important;
    }
    .footer-line {
      width: 85%;
    }
    .block-text {
      margin-top: 20px !important;
      max-width: 290px !important;
      .slogan {
        font-size: 14px !important;
        padding-right: 10px !important;
      }
    }
    .footer-logo {
      display: grid !important;
      text-align: center !important;
      width: 80%;
      margin: 0 auto;
      a {
        order: 2;
        margin-top: 20px;
      }
    }
  }
}
</style>