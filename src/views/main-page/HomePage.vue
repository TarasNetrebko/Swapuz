
<template>
  <MainLayout>
    <template #content>
        <div class="main--wrapper">
        <div class="hero-container">
          <div class="hero">
              <div class="hero-title">
                  <h1>
                      Simple
                      <br>
                      exchange<span class="hero-title-highlight"> 5000+</span> cryptocurrencies
                  </h1>
                  <p class="hero-subtitle">
                      Safely, anonymously and with no limits.
                      <br>
                      Fast crypto swaps with Web3 connection.</p>
              </div>
          </div>
            <div class="exchange">
                <div class="exchange-header">
                    <h2 class="exchange-title">Exchange</h2>
                    <div class="exchange-help">
                        <img src="../../assets/lock.svg" alt="lock">
                        <p>Fixed rate</p>
                        <img src="../../assets/help.svg" alt="help icon">
                    </div>
                </div>
                <div class="exchange-send">
                    <label class="exchange-send-label">
                        <span class="exchange-send-label-title">You send</span>
                        <input type="number" class="exchange-send-input">
                    </label>
                    <div class="exchange-send-currency">
                        <img class="exchange-send-currency-icon" src="" alt="currency icon">
                        <div class="exchange-send-currency-name">
                            <p class="exchange-send-currency-name-abbreviation">BTC</p>
                            <p class="exchange-send-currency-name-abbreviation-2">BNC</p>
                        </div>
                        <img class="exchange-send-currency-arrow" src="../../assets/arrowDownExchange.svg" alt="arrow">
                    </div>
                </div>
                <div class="exchange-middleware">
                    <p class="exchange-middleware-range">Amount range</p>
                    <img class="exchange-middleware-icon" src="../../assets/exchangeIcon.svg" alt="exchange icon">
                </div>
                <div class="exchange-get">
                    <label class="exchange-get-label">
                        <span class="exchange-get-label-title">You get</span>
                        <input type="number" class="exchange-get-input">
                    </label>
                    <div class="exchange-get-currency">
                        <img class="exchange-get-currency-icon" src="" alt="currency icon">
                        <div class="exchange-get-currency-name">
                            <p class="exchange-get-currency-name-abbreviation">ETH</p>
                            <p class="exchange-get-currency-name-abbreviation-2">ERC20</p>
                        </div>
                        <img class="exchange-get-currency-arrow" src="../../assets/arrowDownExchange.svg" alt="arrow">
                    </div>
                </div>
                <div class="exchange-get-single">
                    <p>some wild numbeeeeers</p>
                </div>
                <button class="exchange-button" type="submit">Exchange now</button>
            </div>
            <div class="hero-links">
                <a href="" class="hero-links-trust-pilot">
                    <img src="../../assets/trustpilot.svg" alt="trustpilot">
                    <img src="../../assets/trustpilotStars.svg" alt="trustpilot-stars">
                </a>
                <div class="hero-links-services">
                    <a href="" class="hero-links-google-play">
                        <img src="../../assets/googlePlay.svg" alt="google play">
                    </a>
                    <a href="" class="hero-links-app-store">
                        <img src="../../assets/appStore.svg" alt="app store">
                    </a>
                </div>
            </div>
        </div>
        </div>
    </template>
  </MainLayout>
</template>

<script>
import MainLayout from "../../components/layouts/MainLayout.vue"
export default {
  name: 'HomePage',
    components: { MainLayout },    
}
</script>

<style lang="scss">
@media screen and (min-width: 360px) {
    .main--wrapper {
        width: 100vw;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .hero{
        width: 100%;
        display: flex;
        flex-direction: column;
        &-container {
            padding: 20px 12px 0 12px;
            display: flex;
            flex-wrap: wrap;
            flex-direction: column;
            align-items: center;
            width: 360px;
        }
        &-title {
            width: 100%;
            & h1 {
                display: block;
                width: 100%;
                margin-bottom: 16px;
                color: var(--white-100, #FFF);
                text-align: center;
                font-family: Inter, serif;
                font-size: 36px;
                font-style: normal;
                font-weight: 900;
                line-height: 38px;
                letter-spacing: -0.72px;
            }
            &-highlight {
                color: var(--green, #02C076);
                font-family: Inter, serif;
                font-size: 36px;
                font-style: normal;
                font-weight: 900;
                line-height: 38px;
                letter-spacing: -0.72px;
            }
        }
        &-subtitle {
            display: block;
            width :100%;
            margin-bottom: 24px;
            color: var(--white-100, #FFF);
            text-align: center;
            font-family: Inter, serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 300;
            line-height: 20px;
        }
        &-links {
            margin-top: 40px;
            &-trust-pilot {
                margin-bottom: 24px;
                & img:first-child {
                    margin-right: 8px;
                }
            }
            &-services {
                margin-top: 32px;
                & a:first-child {
                    margin-right: 12px;
                }
            }
        }
    }
    .exchange {
        display: flex;
        flex-direction: column;
        align-items: center;
        order: 0;
        width: 336px;
        height: 332px;
        padding: 16px 12px 22px 12px;
        border-radius: 20px;
        background: var(--gray-card, #29282A);
        backdrop-filter: blur(13.591408729553223px);
        &-header {
            width: 100%;
            padding: 0 12px;
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 24px;
        }
        &-title {
            color: var(--white-100, #FFF);
            font-family: Roboto, serif;
            font-size: 16px;
            font-style: normal;
            font-weight: 900;
            line-height: 24px;
        }
        &-help {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            width: 124px;
            height: 24px;
            cursor: pointer;
            & p {
                color: var(--green, #02C076);
                text-align: center;
                font-family: Inter, serif;
                font-size: 14px;
                font-style: normal;
                font-weight: 700;
                line-height: 24px;
                cursor: pointer;
            }
        }
        &-send {
            width: 100%;
            height: 60px;
            display: flex;
            flex-direction: row;
            align-items: center;
            &-label {
                display: flex;
                flex-direction: column;
                align-items: start;
                padding: 10px 12px 10px 12px;
                width: 294px;
                height: 60px;
                margin-right: 2px;
                border-radius: 8px 0 0 8px;
                background: var(--gray-controls, #363537);
                &-title {
                    color: var(--white-38, rgba(255, 255, 255, 0.38));
                    font-family: Inter, serif;
                    font-size: 12px;
                    font-style: normal;
                    font-weight: 500;
                    line-height: 16px;
                }
            }
            &-input {
                width: 100%;
                height: 24px;
                background-color: transparent;
                border-color: transparent;
                color: var(--white-100, #FFF);
                font-family: Inter, serif;
                font-size: 22px;
                font-style: normal;
                font-weight: 600;
                line-height: 24px;
            }
            &-currency {
                display: flex;
                flex-direction: row;
                align-items: center;
                padding: 12px;
                min-width: 120px;
                height: 60px;
                border-radius: 0 8px 8px 0;
                background: var(--gray-controls, #363537);
                &-icon {
                    display: block;
                    width: 28px;
                    height: 28px;
                    margin-right: 8px;
                    background-color: #FFFFFF;
                }
                &-arrow {
                    display: block;
                    margin-left: auto;
                    width: 12px;
                    height: 24px;
                    cursor: pointer;
                }
                &-name {
                    &-abbreviation {
                        color: var(--white-100, #FFF);
                        font-family: Inter, serif;
                        font-size: 14px;
                        font-style: normal;
                        font-weight: 700;
                        line-height: 20px;
                        &-2 {
                            color: var(--white-38, rgba(255, 255, 255, 0.38));
                            font-family: Inter, serif;
                            font-size: 12px;
                            font-style: normal;
                            font-weight: 500;
                            line-height: 14px;
                        }
                    }
                }
            }
        }
        &-get {
            width: 100%;
            height: 60px;
            display: flex;
            flex-direction: row;
            align-items: center;
            &-label {
                display: flex;
                flex-direction: column;
                align-items: start;
                padding: 10px 12px 10px 12px;
                width: 294px;
                height: 60px;
                margin-right: 2px;
                border-radius: 8px 0 0 8px;
                background: var(--gray-controls, #363537);
                &-title {
                    color: var(--white-38, rgba(255, 255, 255, 0.38));
                    font-family: Inter, serif;
                    font-size: 12px;
                    font-style: normal;
                    font-weight: 500;
                    line-height: 16px;
                }
            }
            &-input {
                width: 100%;
                height: 24px;
                background-color: transparent;
                border-color: transparent;
                color: var(--white-100, #FFF);
                font-family: Inter, serif;
                font-size: 22px;
                font-style: normal;
                font-weight: 600;
                line-height: 24px;
            }
            &-currency {
                display: flex;
                flex-direction: row;
                align-items: center;
                padding: 12px;
                min-width: 120px;
                height: 60px;
                border-radius: 0 8px 8px 0;
                background: var(--gray-controls, #363537);
                &-icon {
                    display: block;
                    width: 28px;
                    height: 28px;
                    margin-right: 8px;
                    background-color: #FFFFFF;
                }
                &-arrow {
                    display: block;
                    margin-left: auto;
                    width: 12px;
                    height: 24px;
                    cursor: pointer;
                }
                &-name {
                    &-abbreviation {
                        color: var(--white-100, #FFF);
                        font-family: Inter, serif;
                        font-size: 14px;
                        font-style: normal;
                        font-weight: 700;
                        line-height: 20px;
                        &-2 {
                            color: var(--white-38, rgba(255, 255, 255, 0.38));
                            font-family: Inter, serif;
                            font-size: 12px;
                            font-style: normal;
                            font-weight: 500;
                            line-height: 14px;
                        }
                    }
                }
            }
            &-single {
                width: 100%;
                height: 48px;
                padding: 8px 12px;
                & p {
                    color: var(--white-100, #FFF);
                    font-family: Inter, serif;
                    font-size: 12px;
                    font-style: normal;
                    font-weight: 500;
                    line-height: 16px;
                }
            }
        }
        &-middleware {
            width: 100%;
            height: 48px;
            padding: 0 6px 0 12px;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            &-range {
                color: var(--white-38, rgba(255, 255, 255, 0.38));
                font-family: Inter, serif;
                font-size: 12px;
                font-style: normal;
                font-weight: 500;
                line-height: 16px;
                margin-top: 8px;
            }
            &-icon {
                width: 24px;
                height: 24px;
                margin: auto 0;
                cursor: pointer;
            }
        }
        &-button {
            width:100%;
            display: flex;
            height: 60px;
            justify-content: center;
            align-items: center;
            gap: 10px;
            border-radius: 8px;
            background: var(--green, #02C076);
            backdrop-filter: blur(13.591408729553223px);
            color: var(--gray-card, #29282A);
            text-align: center;
            font-family: Inter, serif;
            font-size: 16px;
            font-style: normal;
            font-weight: 700;
            line-height: 24px;
            cursor: pointer;
        }
    }
}
@media screen and (min-width: 1200px) {
    .hero {
        width: 520px;
      &-container {
        margin: 0 auto;
        padding: 88px 0 0 0;
        width: 1080px;
        flex-direction: row;
        align-items: flex-start;
      }
      &-title {
        width: 520px;
        & h1 {
          display: block;
          width: 100%;
          margin-bottom: 24px;
            text-align: start;
          color: #FFF;
          font-family: Inter, serif;
          font-size: 56px;
          font-style: normal;
          font-weight: 900;
          line-height: 62px;
          letter-spacing: -1.12px;
        }
        &-highlight {
          color: #02C076;
          font-family: Inter, serif;
          font-size: 56px;
          font-style: normal;
          font-weight: 900;
          line-height: 62px;
          letter-spacing: -1.12px;
        }
      }
      &-subtitle {
        display: block;
        width :100%;
        color: #FFF;
        margin-bottom: 0;
          text-align: start;
        font-family: Inter, serif;
        font-size: 20px;
        font-style: normal;
        font-weight: 300;
        line-height: 28px;
      }
      &-links {
          margin-top: -74px;
          &-trust-pilot {
              margin-bottom: 32px;
              & img:first-child {
                  margin-right: 8px;
              }
          }
          &-services {
              margin-top: 32px;
              & a:first-child {
                  margin-right: 12px;
              }
          }
      }
    }
    .exchange {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 520px;
        height: 396px;
        margin-left: 40px;
        padding: 28px 44px 44px 44px;
        border-radius: 20px;
        background: var(--gray-card, #29282A);
        backdrop-filter: blur(13.591408729553223px);
        &-header {
            width: 100%;
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 24px;
        }
        &-title {
            color: var(--white-100, #FFF);
            font-family: Roboto, serif;
            font-size: 24px;
            font-style: normal;
            font-weight: 900;
            line-height: 24px;
        }
        &-help {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            width: 124px;
            height: 24px;
            cursor: pointer;
            & p {
                color: var(--green, #02C076);
                text-align: center;
                font-family: Inter, serif;
                font-size: 14px;
                font-style: normal;
                font-weight: 700;
                line-height: 24px;
                cursor: pointer;
            }
        }
        &-send {
            width: 100%;
            height: 60px;
            display: flex;
            flex-direction: row;
            align-items: center;
            &-label {
                display: flex;
                flex-direction: column;
                align-items: start;
                padding: 10px 12px 10px 12px;
                width: 294px;
                height: 60px;
                margin-right: 2px;
                border-radius: 8px 0 0 8px;
                background: var(--gray-controls, #363537);
                &-title {
                    color: var(--white-38, rgba(255, 255, 255, 0.38));
                    font-family: Inter, serif;
                    font-size: 12px;
                    font-style: normal;
                    font-weight: 500;
                    line-height: 16px;
                }
            }
            &-input {
                width: 100%;
                height: 24px;
                background-color: transparent;
                border-color: transparent;
                color: var(--white-100, #FFF);
                font-family: Inter, serif;
                font-size: 22px;
                font-style: normal;
                font-weight: 600;
                line-height: 24px;
            }
            &-currency {
                display: flex;
                flex-direction: row;
                align-items: center;
                padding: 12px 12px 12px 16px;
                width: 136px;
                height: 60px;
                border-radius: 0 8px 8px 0;
                background: var(--gray-controls, #363537);
                &-icon {
                    display: block;
                    width: 28px;
                    height: 28px;
                    margin-right: 8px;
                    background-color: #FFFFFF;
                }
                &-arrow {
                    width: 24px;
                }
                &-name {
                    &-abbreviation {
                        color: var(--white-100, #FFF);
                        font-family: Inter, serif;
                        font-size: 14px;
                        font-style: normal;
                        font-weight: 700;
                        line-height: 20px;
                        &-2 {
                            color: var(--white-38, rgba(255, 255, 255, 0.38));
                            font-family: Inter, serif;
                            font-size: 12px;
                            font-style: normal;
                            font-weight: 500;
                            line-height: 14px;
                        }
                    }
                }
            }
        }
        &-get {
            width: 100%;
            height: 60px;
            display: flex;
            flex-direction: row;
            align-items: center;
            &-label {
                display: flex;
                flex-direction: column;
                align-items: start;
                padding: 10px 12px 10px 12px;
                width: 294px;
                height: 60px;
                margin-right: 2px;
                border-radius: 8px 0 0 8px;
                background: var(--gray-controls, #363537);
                &-title {
                    color: var(--white-38, rgba(255, 255, 255, 0.38));
                    font-family: Inter, serif;
                    font-size: 12px;
                    font-style: normal;
                    font-weight: 500;
                    line-height: 16px;
                }
            }
            &-input {
                width: 100%;
                height: 24px;
                background-color: transparent;
                border-color: transparent;
                color: var(--white-100, #FFF);
                font-family: Inter, serif;
                font-size: 22px;
                font-style: normal;
                font-weight: 600;
                line-height: 24px;
            }
            &-currency {
                display: flex;
                flex-direction: row;
                align-items: center;
                padding: 12px 12px 12px 16px;
                width: 136px;
                height: 60px;
                border-radius: 0 8px 8px 0;
                background: var(--gray-controls, #363537);
                &-icon {
                    display: block;
                    width: 28px;
                    height: 28px;
                    margin-right: 8px;
                    background-color: #FFFFFF;
                }
                &-arrow {
                    width: 24px;
                }
                &-name {
                    &-abbreviation {
                        color: var(--white-100, #FFF);
                        font-family: Inter, serif;
                        font-size: 14px;
                        font-style: normal;
                        font-weight: 700;
                        line-height: 20px;
                        &-2 {
                            color: var(--white-38, rgba(255, 255, 255, 0.38));
                            font-family: Inter, serif;
                            font-size: 12px;
                            font-style: normal;
                            font-weight: 500;
                            line-height: 14px;
                        }
                    }
                }
            }
            &-single {
                width: 100%;
                height: 48px;
                padding: 8px 12px;
                & p {
                    color: var(--white-100, #FFF);
                    font-family: Inter, serif;
                    font-size: 12px;
                    font-style: normal;
                    font-weight: 500;
                    line-height: 16px;
                }
            }
        }
        &-middleware {
            width: 100%;
            height: 48px;
            padding: 0 12px;
            &-range {
                color: var(--white-38, rgba(255, 255, 255, 0.38));
                font-family: Inter, serif;
                font-size: 12px;
                font-style: normal;
                font-weight: 500;
                line-height: 16px;
                margin-top: 8px;
            }
            &-icon {
                width: 24px;
                height: 24px;
                margin: auto 0;
                cursor: pointer;
            }
        }
        &-button {
            width:100%;
            display: flex;
            text-align: center;
            font-size: 18px;
            cursor: pointer;
        }
    }
}
</style>

