<template>
<!--    ///-->
<!--    Mobile version below-->
<!--    ///-->
    <div class="mob-header">
        <div class="menu-button--wrapper">
                <div class="menu-button" :class="{ 'menu-button--active': isDropMenu }" @click="isDropMenu = true">
                    <img src="../assets/menu-button.svg" alt="menu-button">
                </div>
        </div>
        <div v-if="isDropMenu" class="drop-menu" :class="{'drop-menu--closed': isDropMenu}" >
            <div class="drop-menu-head">
                    <div class="drop-menu-head-country--wrapper" :class="{ 'nav-link--active': isDropCountry }" @click="isDropCountry = !isDropCountry">
                        <div class="drop-menu-head-country-flag"></div>
                        Poland
                        <img src="../assets/arrowDown.svg" alt="option-button" />
                        <div v-if="isDropCountry" class="drop-select">
                            <p>England</p>
                            <p>France</p>
                            <p>Ukraine</p>
                        </div>
                    </div>
                <button type="button" class="drop-menu-head-close" @click="isDropMenu = false; isDropCountry = false; isDropPartners = false">
                    <img class="drop-menu-head-close-cross" src="../assets/closeCross.svg" alt="close">
                </button>
            </div>
            <nav class="drop-menu-nav">
                <a href="" class="drop-menu-nav-link">Main</a>
                <a href="" class="drop-menu-nav-link">About</a>
                <a href="" class="drop-menu-nav-link">Contacts</a>
                <div class="drop-menu-nav-link" :class="{ 'nav-link--active': isDropPartners }" @click="isDropPartners = !isDropPartners">
                    Partners
                    <img src="../assets/arrowDown.svg" alt="option-button" />
                </div>
                <div v-if="isDropPartners" class="drop-menu-nav-optional">
                    <a class="drop-menu-nav-optional-link" href="">Affiliate program</a>
                    <a class="drop-menu-nav-optional-link" href="">
                        API Documentation
                        <div class="drop-menu-nav-optional-link-mark">
                            New
                        </div>
                    </a>
                </div>
                <a href="" class="drop-menu-nav-link">Support</a>
                <a href="" class="drop-menu-nav-link">How to use</a>
            </nav>
            <div class="drop-menu-footer">
                <button class="drop-menu-footer-auth" type="button">
                    Log in
                    <img src="../assets/mobAuth.svg" alt="auth">
                </button>
            </div>
        </div>
        <div class="logo-header">
            <img src="../assets/logo-mob-header.svg" alt="logo" />
        </div>
            <div class="nav-link mob-country-link" :class="{ 'nav-link--active': isDropCountry }" @click="isDropCountry = !isDropCountry">
                <div class="country-flag"></div>
                PL
            </div>
    </div>
<!--///-->
<!--Desktop version below-->
<!--///-->
    <div class="desk-header">
        <div class="logo-header">
            <img src="../assets/logo-desktop.svg" alt="logo" />
        </div>
        <div class="country-switcher">
            <div class="nav-link" :class="{ 'nav-link--active': isDropCountry }" @click="isDropCountry = !isDropCountry">
                <div class="country-flag"></div>
                Poland
                <img src="../assets/arrowDown.svg" alt="option-button" />
                <div v-if="isDropCountry" class="drop-select">
                    England
                    France
                    Ukraine
                </div>
            </div>
        </div>
        <nav class="nav">
            <a href="" class="nav-link">How to use</a>
            <a href="" class="nav-link">About</a>
            <div class="nav-link" :class="{'nav-link--active': isDropSupport}" @click="isDropSupport = !isDropSupport">
                Support
                <img src="../assets/arrowDown.svg" alt="option-button"/>
                <div v-if="isDropSupport" class="drop-select">
                    test
                </div>
            </div>
            <a href="" class="nav-link">Contact</a>
            <div class="nav-link" :class="{ 'nav-link--active': isDropPartners }" @click="isDropPartners = !isDropPartners">
                Partners
                <img src="../assets/arrowDown.svg" alt="option-button" />
                <div v-if="isDropPartners" class="drop-select">
                    test
                </div>
            </div>
        </nav>
        <button type="button" class="auth-button">
            Log in
            <img src="../assets/auth.svg" alt="auth icon" />
        </button>
    </div>
</template>
<script>
export default {
  name: 'HeaderComp',
  data() {
    return {
        isDropSupport: false,
        isDropPartners: false,
        isDropCountry: false,
        isDropMenu: false,
    }
  }
}
</script>
<style lang="scss">
@media screen and (min-width: 320px) {
  .desk-header {
    display: none;
  }
  .mob-header {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100vw;
    height: 64px;
    color: #fff;
  }
  .menu-button {
      display: flex;
      flex-direction: row;
      align-items: center;
    background: #29282A;
      cursor: pointer;
    &--wrapper {
        width: 40px;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 8px;
        background: #29282A;
        margin-left: 12px;
    }
  }
  .country-flag {
    width: 16px;
    height: 12px;
    margin-right: 8px;
    background-color: white;
  }
  .logo-header {
    margin-bottom: 2px;
  }
  .nav-link {
      color: #fff;
      margin-bottom: 5px;
  }
  .mob-country-link {
      display: flex;
      flex-direction: row;
      align-items: center;
      position: relative;
      color: #fff;
    margin-right: 20px;
  }
  .drop-select {
    position: absolute;
      width: 100%;
    top: calc(100% + 5px);
    left: 0;
    z-index: 3;
      display: flex;
      flex-direction: column;
      & p {
          display: block;
          text-align: center;
      }
  }
  .drop-menu {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        position: absolute;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        z-index: 2;
        background: #1B1A1C;
        &-footer {
            padding: 16px;
            height: 80px;
            width: 100%;
            &-auth {
                display: flex;
                align-items: center;
                justify-content: center;
                height: 48px;
                width: 100%;
                border-radius: 8px;
                background: #02C076;
                color: #1B1A1C;
                text-align: center;
                font-family: Inter, serif;
                font-size: 14px;
                font-style: normal;
                font-weight: 700;
                line-height: 20px;
                cursor: pointer;
                & img {
                    margin-left: 8px;
                }
            }
        }
        &-head {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            width: 100%;
            height: 64px;
            padding: 12px;
            &-country--wrapper {
                display: flex;
                flex-direction: row;
                align-items: center;
                position: relative;
                height: 40px;
                padding: 0 16px;
                border-radius: 8px;
                background: var(--gray-card, #29282A);
                color: #FFF;
                font-family: Inter, serif;
                font-size: 14px;
                font-style: normal;
                font-weight: 700;
                line-height: 24px;
                cursor: pointer;
                & img {
                    margin-left: 2px;
                }
            }
            &-close {
                width: 40px;
                height: 40px;
                display: flex;
                align-items: center;
                justify-content: center;
                border-radius: 8px;
                background: var(--gray-card, #29282A);
            }
            &-country-flag {
                width: 16px;
                height: 12px;
                margin-right: 12px;
                background-color: #fff;
            }
        }
        &-nav {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            &-link {
                color: #FFF;
                font-family: Inter, serif;
                font-size: 20px;
                font-style: normal;
                font-weight: 700;
                line-height: 24px;
                cursor: pointer;
                &:not(:last-child) {
                    margin-bottom: 32px;
                }
            }
            &-optional {
                width: 100%;
                height: 88px;
                &-link {
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    justify-content: center;
                    margin-bottom: 20px;
                    color: rgba(255, 255, 255, 0.72);
                    text-align: center;
                    font-family: Inter, serif;
                    font-size: 14px;
                    font-style: normal;
                    font-weight: 600;
                    line-height: 24px;
                    cursor: pointer;
                    &-mark {
                        text-align: center;
                        font-family: Inter, serif;
                        font-size: 12px;
                        font-style: normal;
                        font-weight: 700;
                        line-height: 16px;
                        margin-left: 10px;
                        padding: 1px 4px;
                        border-radius: 4px;
                        background: #FF783E;
                        color: #29282A;
                    }
                }
            }
        }
  }
}
@media screen and (min-width: 1200px) {
    .mob-header {
      display: none;
    }
    .desk-header {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      width: 100vw;
      height: 96px;
      padding: 0 140px;
      color: #fff;
      font-family: Inter, serif;
      font-size: 14px;
      font-style: normal;
      font-weight: 700;
      line-height: 24px;
    }
    .logo-header {
      margin: 24px 0 36px 0;
        cursor: pointer;
    }
    .country-switcher {
      display: flex;
      flex-direction: row;
      align-items: center;
      margin-left: 36.06px;
        cursor: pointer;
    }
    .nav {
      display: flex;
      flex-direction: row;
      align-items: center;
      margin-left: 50px;
        &-link {
            display: flex;
            flex-direction: row;
            align-items: center;
            position: relative;
            color: white;
            &:not(:first-child) {
                margin-left: 40px;
            }
            &--active {
                img {
                    transform: rotate(-180deg);
                }
            }
        }
    }
    .drop-select {
      position: absolute;
      top: calc(100% + 5px);
      left: 0;
    }
    .country-flag {
      display: block;
      margin-right: 11px;
    }
    .auth-button {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      margin-left: auto;
      height: 40px;
      padding: 16px;
      gap: 8px;
      flex-shrink: 0;
      border-radius: 8px;
      background: var(--gray-controls, #363537);
      backdrop-filter: blur(13.591408729553223px);
      color: var(--green, #02c076);
      text-align: center;
      font-family: Inter, serif;
      font-size: 14px;
      font-style: normal;
      font-weight: 700;
      line-height: 20px;
        cursor: pointer;
    }
  }
</style>
