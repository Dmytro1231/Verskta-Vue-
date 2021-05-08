<template>
  <div class="container">
    <div class="container-top">
      <div class="wrapper-top">
        <img
          src="../assets/trader.jpg"
          alt="trader"
          width="632"
          height="360"
          class="trader"
        />
        <img
          src="../assets/trader-mobile.jpg"
          alt="trader"
          width="320"
          height="234"
          class="mobile-trader"
        />
        <div class="schedule-block">
          <h3 class="title-schedule">
            Boost your day trading experience with Tradenet Plus
          </h3>
          <ol>
            <li>
              Get your hands-on day trading experience with a simulated demo
              account without risking any money
            </li>
            <li>
              Take your first trading steps in a safe environment and follow
              trades by experienced day traders in the chat room
            </li>
            <li>Ask your questions and get feedback from top traders</li>
          </ol>
        </div>
      </div>
    </div>
    <div class="container-bottom">
      <h2 class="title-rates">Tradenet Plus</h2>
      <div class="rates-block-wrapper">
        <div class="rate-block">
          <div class="wrapper-rate">
            <div class="left-block">
              <h4 class="title">Simulated Demo Account</h4>
              <ul>
                <li>$80,000 training account</li>
                <li>Maximum drawdown $4,000</li>
                <li>MTS included</li>
                <li>One month access</li>
              </ul>
            </div>
            <div class="right-block">
              <img
                src="../assets/macbook.png"
                alt="Free-Macbook-Air-2020"
                class="left-mac"
                width="170"
                height="220"
              />
              <img
                src="../assets/macbook-mobile.png"
                alt="Free-Macbook-Air-2020"
                class="left-mac-mobile"
                width="100"
                height="130"
              />
            </div>
          </div>
          <hr class="horizontal-line" />
          <div class="mobile-block">
            <h3 class="title">How it works?</h3>
            <ul>
              <li>You can lose up to $4,000 on the demo account</li>
              <li>
                If you exceed the maximum loss, your account will be restored
                within a week.
              </li>
              <li>
                You can restore your account unlimited number of times but only
                on a given weekday
              </li>
              <li>
                With MTS included you will have full history and access to your
                trade statistics
              </li>
            </ul>
          </div>
        </div>
        <div>
          <p class="plus">+</p>
        </div>
        <div class="rate-block">
          <div class="wrapper-rate reverse">
            <div class="left-block">
              <h4 class="title">Live Trading Chat Room</h4>
              <ul>
                <li>Live every trading day</li>
                <li>Watch and follow trades<span>by top traders</span></li>
                <li>Ask your questions and get detailed answers</li>
                <li>One month access</li>
              </ul>
            </div>
            <div class="right-block reverse">
              <img
                src="../assets/macbook2.png"
                alt="Free-Macbook-Air-2020"
                class="right-mac"
                width="170"
                height="220"
              />
              <img
                src="../assets/macbook-mobile2.png"
                alt="Free-Macbook-Air-2020"
                class="right-mac-mobile"
                width="100"
                height="130"
              />
            </div>
          </div>
          <hr class="horizontal-line" />
          <div class="mobile-block">
            <h3 class="title">How it works?</h3>
            <ul>
              <li>
                You can watch professionals in the chat room and get access to
                their insights and input every day between 9:30am and 4pm every
                trading day
              </li>
              <li>
                No latency, you can watch the traders as they click on the “Buy”
                and “Sell” buttons
              </li>
              <li>
                You can restore your account unlimited number of times but only
                on a given weekday
              </li>
              <li>
                Become a part of a community of day traders who support,
                discuss, and encourage one another.
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="block-slug">
        <h2 class="slug">FOR FREE!</h2>
        <span>Limited time offer</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  padding-top: 80px;
  .wrapper-top {
    display: flex;
    justify-content: center;
    flex-direction: row;
    margin-left: 157px;
    .mobile-trader {
      display: none;
    }
    .schedule-block {
      width: 618px;
      height: 291px;
      background: #ffffff;
      box-shadow: 0px 9px 90px rgba(0, 0, 0, 0.25);
      border-radius: 2px;
      position: relative;
      right: 140px;
      top: 35px;
      padding: 40px;
      .title-schedule {
        margin-bottom: 20px;
        font-weight: bold;
        font-size: 24px;
        line-height: 28px;
      }
      ol {
        margin-left: 30px;
        width: 480px;
        list-style: decimal-leading-zero;
      }
      li::marker {
        color: #5a17ff;
      }
      ol li:not(:last-child) {
        margin-bottom: 20px;
      }
    }
  }
  .container-bottom {
    background: #f1f2f4;
    margin-top: 80px;
    padding-top: 80px;
    padding-bottom: 80px;
    .title-rates {
      font-weight: 500;
      font-size: 40px;
      line-height: 47px;
      text-align: center;
      margin-bottom: 40px;
    }
    .rates-block-wrapper {
      display: flex;
      justify-content: center;
      color: #fff;
      align-items: center;
      .plus {
        padding: 5px;
        color: #5a17ff;
        font-size: 48px;
        line-height: 57px;
        margin: 0 20px 0 20px;
      }
      .rate-block {
        background: #4c1ed3;
        box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.25);
        border-radius: 5px;
        width: 520px;
        .wrapper-rate {
          display: flex;
          flex-direction: row;
          width: 520px;
          height: 337px;
          padding-top: 50px;
          padding-left: 40px;
          padding-bottom: 80px;
          justify-content: flex-end;
          .left-block {
            .title {
              font-weight: bold;
              font-size: 24px;
              line-height: 28px;
              margin-bottom: 20px;
            }
            ul {
              margin-left: 20px;
              li {
                font-size: 20px;
                line-height: 24px;
                width: 274px;
                &:not(:last-child) {
                  margin-bottom: 15px;
                }
                span {
                  display: block;
                }
              }
            }
          }
          .right-block {
            .left-mac-mobile {
              display: none;
            }
          }
        }
        .wrapper-rate.reverse {
          flex-direction: row-reverse;
          justify-content: flex-end;
          padding-left: 0;
          .right-mac-mobile {
            display: none;
          }
        }
      }
      .mobile-block {
        display: none;
      }
    }
  }
  .block-slug {
    text-align: center;
    margin-top: 40px;
    .slug {
      color: #1bd895;
      font-weight: bold;
      font-size: 32px;
      line-height: 38px;
    }
    span {
      font-size: 14px;
      line-height: 17px;
    }
  }
}
@media (max-width: 320px) {
  .wrapper-top {
    flex-direction: column !important;
    margin-left: 0 !important;
    .trader {
      display: none;
    }
    .mobile-trader {
      display: block !important;
    }
    .schedule-block {
      width: 290px !important;
      height: 366px !important;
      padding: 30px 14px 20px 14px !important;
      right: 0 !important;
      top: -110px !important;
      left: 15px;
      .title-schedule {
        font-size: 20px !important;
        line-height: 24px !important;
      }
      ol {
        width: 230px !important;
        li {
          margin-bottom: 10px !important;
        }
      }
    }
  }
  .container-bottom {
    margin-top: 0 !important;
    padding-top: 35px !important;
    .title-rates {
      font-size: 32px !important;
      text-align: left !important;
      margin-left: 10px !important;
    }
    .rates-block-wrapper {
      flex-direction: column !important;
      .rate-block {
        width: 290px !important;
        height: 100% !important;
        .horizontal-line {
          width: 90%;
          margin: 0 auto;
        }
        .wrapper-rate {
          padding-top: 20px !important;
          padding-bottom: 10px !important;
          width: 100% !important;
          height: 100% !important;
          .right-block {
            display: flex !important;
            justify-content: flex-end !important;
            align-items: center !important;
          }
          .left-block {
            .title {
              font-size: 20px !important;
            }
            ul li {
              font-size: 16px !important;
              width: 135px !important;
            }
          }
          .right-block {
            .left-mac {
              display: none;
            }
            .left-mac-mobile {
              display: block !important;
            }
          }
        }
        .wrapper-rate.reverse {
          .right-mac {
            display: none;
          }
          .right-mac-mobile {
            display: block !important;
          }
        }
      }
      .mobile-block {
        display: flex !important;
        order: 3;
        flex-direction: column !important;
        padding-bottom: 40px;
        margin-left: 30px;
        .title {
          font-size: 24px;
          line-height: 28px;
          margin-top: 20px;
          margin-bottom: 20px;
        }
        ul li {
          font-weight: normal;
          font-size: 16px;
          line-height: 19px;
          max-width: 250px;
        }
        ul li:not(:last-child) {
          margin-bottom: 10px;
        }
      }
    }
  }
}
</style>