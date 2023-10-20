
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
                  <a href="" class="hero-trust-pilot">
                      <img src="../../assets/trustpilot.svg" alt="trustpilot">
                      <img src="../../assets/trustpilotStars.svg" alt="trustpilot-stars">
                  </a>
                  <div class="hero-links">
                      <a href="" class="hero-links-google-play">
                          <img src="../../assets/googlePlay.svg" alt="google play">
                      </a>
                      <a href="" class="hero-links-app-store">
                          <img src="../../assets/appStore.svg" alt="app store">
                      </a>
                  </div>
          </div>
            <div class="exchange">
                <div class="exchange-header">
                    <h2 class="exchange-title">Exchange</h2>
                    <div class="exchange-help">
                        wewr
                        erwe
                        wer
                    </div>
                </div>
                <div class="exchange-send">
                    <input type="number" class="exchange-send-input">
                    <div class="exchange-send-currency"></div>
                </div>
                <div class="exchange-middleware">
                    <p class="exchange-middleware-range">Amount range</p>
                    <img class="exchange-middleware-icon" src="../../assets/exchangeIcon.svg" alt="exchange icon">
                </div>
                <div class="exchange-get">
                    <input type="number" class="exchange-get-input">
                    <div class="exchange-get-currency"></div>
                </div>
                <div class="exchange-get-single">
                    <p>sdfsfsdf</p>
                </div>
                <button class="exchange-button" type="submit">Exchange now</button>
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
@media screen and (min-width: 1200px) {
    .main--wrapper {
        width: 100vw;
    }
    .hero {
       width: 100%;
       display: flex;
       flex-direction: column;
      &-container {
        margin: 0 auto;
        padding: 88px 0 0 0;
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 1080px;
      }
      &-title {
        width: 520px;
        & h1 {
          display: block;
          width: 100%;
          margin-bottom: 24px;
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
        margin-bottom: 50px;
        color: #FFF;
        font-family: Inter, serif;
        font-size: 20px;
        font-style: normal;
        font-weight: 300;
        line-height: 28px;
      }
      &-trust-pilot {
          margin-bottom: 32px;
          & img:first-child {
              margin-right: 8px;
          }
      }
      &-links {
          & a:first-child {
              margin-right: 12px;
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
        &-send {
            width: 100%;
            height: 60px;
            display: flex;
            flex-direction: row;
            align-items: center;
            &-input {
                width: 294px;
                height: 60px;
                margin-right: 2px;
                border-radius: 8px 0 0 8px;
                background: var(--gray-controls, #363537);
            }
            &-currency {
                width: 136px;
                height: 60px;
                border-radius: 0 8px 8px 0;
                background: var(--gray-controls, #363537);
            }
        }
        &-get {
            width: 100%;
            height: 60px;
            display: flex;
            flex-direction: row;
            align-items: center;
            &-input {
                width: 294px;
                height: 60px;
                margin-right: 2px;
                border-radius: 8px 0 0 8px;
                background: var(--gray-controls, #363537);
            }
            &-currency {
                width: 136px;
                height: 60px;
                border-radius: 0 8px 8px 0;
                background: var(--gray-controls, #363537);
            }
            &-single {
                width: 100%;
                height: 48px;
                padding: 8px 12px;
            }
        }
        &-middleware {
            width: 100%;
            height: 48px;
            padding: 0 12px;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            &-range {
                margin-top: 8px;
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
            color: #29282A;
            text-align: center;
            font-family: Inter, serif;
            font-size: 18px;
            font-style: normal;
            font-weight: 700;
            line-height: 24px;
        }
    }
}
</style>

