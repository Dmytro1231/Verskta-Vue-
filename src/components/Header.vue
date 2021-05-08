<template>
  <div class="container">
    <div class="wrapper">
      <div class="block-title">
        <h1 class="title">Tradenet Plus</h1>
        <p class="subtitle">
          One month access to Tradenet day trading chat room and demo training
          account
        </p>
        <p class="slug">FOR FREE!</p>
        <span class="slug-subtitle">Limited time offer</span>
        <button class="btn">GET NOW</button>
      </div>
      <div class="img-block">
        <img
          src="../assets/header-image.png"
          alt="header-img"
          width="536"
          height="384"
          class="desktop"
        />
        <img
          src="../assets/header-mobile.png"
          alt="header-img"
          width="280"
          height="180"
          class="mobile"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  background: url("../assets/bg-header.png") no-repeat 100% 100%;
  background-size: cover;
  .wrapper {
    margin: 0 auto;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    color: #fff;
    padding-top: 70px;
    padding-bottom: 182px;
    .block-title {
      margin-right: 72px;
      margin-top: 80px;
      .title {
        font-weight: 500;
        font-size: 64px;
        line-height: 76px;
        margin-bottom: 20px;
        letter-spacing: 1.5px;
      }
      .subtitle {
        font-weight: normal;
        font-size: 24px;
        max-width: 482px;
        line-height: 28px;
        margin-bottom: 40px;
      }
      .slug {
        color: #1bd895;
        font-weight: bold;
        font-size: 24px;
        margin-bottom: 8px;
      }
      .slug-subtitle {
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 17px;
      }
    }
    .img-block {
      margin-top: 38px;
      .desktop {
        object-fit: contain;
      }
      .mobile {
        display: none;
      }
    }
  }
}
@media (max-width: 320px) {
  .container {
    background-image: url("../assets/mobile.bg.png") no-repeat 100% 100%;
    .wrapper {
      flex-direction: column;
      padding-top: 0;
      padding-bottom: 0;
      .block-title {
        margin-top: 0;
        margin-right: 0;
        order: 2;
        text-align: center;
        .title {
          font-size: 36px;
          line-height: 43px;
        }
        .subtitle {
          font-size: 20px;
          line-height: 24px;
          max-width: 290px;
          margin-bottom: 20px;
        }
        .slug {
          margin-bottom: 3px;
        }
        .btn {
          margin: 33px auto 60px auto;
          padding: 18px 95px 18px 95px;
        }
      }
      .img-block {
        margin-top: 50px;
        margin-bottom: 60px;
        .desktop {
          display: none;
        }
        .mobile {
          display: block;
        }
      }
    }
  }
}
</style>