<template>
<!--    ///-->
<!--    Mobile version below-->
<!--    ///-->
    <div class="mob-header">
        <div class="menu-button--wrapper">
                <div class="menu-button" :class="{ 'menu-button--active': isDropMenu }" @click="isDropMenu = !isDropMenu">
                    <img src="../assets/menu-button.svg" alt="menu-button">
                    <div v-if="isDropMenu" class="drop-menu" >
                        <a href="" class="nav-link">How to use</a>
                        <a href="" class="nav-link">About</a>
                        <a href="" class="nav-link">Support</a>
                        <a href="" class="nav-link">Contact</a>
                    </div>
                </div>
        </div>
        <div class="logo-header">
            <img src="../assets/logo-mob-header.svg" alt="logo" />
        </div>
            <div class="nav-link mob-country-link" :class="{ 'nav-link--active': isDropCountry }" @click="isDropCountry = !isDropCountry">
                <div class="country-flag"></div>
                PL
                <div v-if="isDropCountry" class="drop-select">
                    UK
                    FR
                    UKR
                </div>
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
        isDropMenu: false
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
  .menu-button--wrapper {
    width: 40px;
    height: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 8px;
    background: #29282A;
    margin-left: 12px;
  }
  .menu-button {
    background: #29282A;
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
    top: calc(100% + 5px);
    left: 0;
  }
  .menu-button {
        display: flex;
        flex-direction: row;
        align-items: center;
        position: relative;
  }
    .drop-menu {
        display: flex;
        flex-direction: column;
        position: absolute;
        top: 0;
        left: calc(100% + 5px);
        min-width: 100px;
    }
}
@media screen and (min-width: 1280px) {
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
    }
    .country-switcher {
      display: flex;
      flex-direction: row;
      align-items: center;
      margin-left: 36.06px;
    }
    .nav {
      display: flex;
      flex-direction: row;
      align-items: center;
      margin-left: 50px;
    }
  .nav-link {
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
    }
  }
</style>
