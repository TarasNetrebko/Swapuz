<template>
<!--    DESKTOP VERSION-->
        <div class="footer desk">
            <div class="container">
                <div class="useful-information">
                    <section class="company-introduce">
                        <div class="logo-footer">
                            <img class="logo-desk-footer" src="../assets/logo-desktop.svg" alt="logo" />
                        </div>
                        <p class="text-call">
                            Do you want to make operations with Swapuz as handy as possible? Add it to bookmarks
                            in one click!
                        </p>
                    </section>
                    <section class="contacts">
                        <div class="contacts-links-container">
                            <b class="contacts-header">Company</b>
                            <ul class="contacts-links">
                                <li class="contacts-link">
                                    <a href="">About</a>
                                </li>
                                <li class="contacts-link">
                                    <a href="">Contacts</a>
                                </li>
                            </ul>
                        </div>
                        <div class="contacts-links-container">
                            <b class="contacts-header">Support</b>
                            <ul class="contacts-links">
                                <li class="contacts-link">
                                    <a href="">How to use</a>
                                </li>
                                <li class="contacts-link">
                                    <a href="">Youtube tutorial</a>
                                </li>
                                <li class="contacts-link">
                                    <a href="">FAQ</a>
                                </li>
                            </ul>
                        </div>
                        <div class="contacts-links-container">
                            <b class="contacts-header">Follow Us</b>
                            <ul class="social-networks">
                                <li class="social-link">
                                    <a href=""><img src="../assets/discordIcon.svg" alt="discord" /></a>
                                </li>
                                <li class="social-link">
                                    <a href=""><img src="../assets/twitterIcon.svg" alt="twitter" /></a>
                                </li>
                                <li class="social-link">
                                    <a href=""><img src="../assets/telegramIcon.svg" alt="telegram" /></a>
                                </li>
                                <li class="social-link">
                                    <a href=""><img src="../assets/youtubeIcon.svg" alt="youtube" /></a>
                                </li>
                            </ul>
                        </div>
                    </section>
                </div>
                <div class="rights">
                    <p class="copyright">Copyright &copy; 2020 - 2021 Swapuz!</p>
                    <div class="rights-link">
                        <a href="">Term of Use</a>
                        <div class="underline-term"></div>
                    </div>
                    <div class="rights-link">
                        <a href="">Privacy Policy</a>
                        <div class="underline-policy"></div>
                    </div>
                </div>
        </div>
    </div>
<!--    MOBILE VERSION-->
    <div class="footer mob">
        <div class="container">
                <div class="logo-footer">
                    <img class="logo-mob-footer" src="../assets/logo-mob-footer.svg" alt="logo">
                </div>
                <p class="text-call">
                    Do you want to make operations with Swapuz as handy as possible? Add it to bookmarks
                    in one click!
                </p>
            <section class="contacts">
                <div class="contacts-links-container socials">
                    <b class="contacts-header">Follow Us</b>
                    <ul class="social-networks">
                        <li class="social-link">
                            <a href=""><img src="../assets/discordIcon.svg" alt="discord" /></a>
                        </li>
                        <li class="social-link">
                            <a href=""><img src="../assets/twitterIcon.svg" alt="twitter" /></a>
                        </li>
                        <li class="social-link">
                            <a href=""><img src="../assets/telegramIcon.svg" alt="telegram" /></a>
                        </li>
                        <li class="social-link">
                            <a href=""><img src="../assets/youtubeIcon.svg" alt="youtube" /></a>
                        </li>
                    </ul>
                </div>
                <div class="contacts-links--wrapper">
                    <div class="contacts-links-container company-links">
                        <b class="contacts-header">Company</b>
                        <ul class="contacts-links">
                            <li class="contacts-link">
                                <a href="">About</a>
                            </li>
                            <li class="contacts-link">
                                <a href="">Contacts</a>
                            </li>
                        </ul>
                    </div>
                    <div class="contacts-links-container company-links">
                        <b class="contacts-header">Support</b>
                        <ul class="contacts-links">
                            <li class="contacts-link">
                                <a href="">How to use</a>
                            </li>
                            <li class="contacts-link">
                                <a href="">Youtube tutorial</a>
                            </li>
                            <li class="contacts-link">
                                <a href="">FAQ</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </section>
            <div class="rights">
                <p class="copyright">Copyright &copy; 2020 - 2021 Swapuz!</p>
                <div class="rights-links--wrapper">
                    <div class="rights-link">
                        <a href="">Term of Use</a>
                        <div class="underline-term"></div>
                    </div>
                    <div class="rights-link">
                        <a href="">Privacy Policy</a>
                        <div class="underline-policy"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
  export default {
    name: 'FooterComp'
  }
</script>
<style lang="scss">
@media screen and (min-width: 320px) {
    .mob {
        display: flex;
        padding-top: 32px;
    }
    .desk {
        display: none;
    }
    .footer {
        width: 100vw;
        border-radius: 24px 24px 0 0;
        background: #29282a;
    }
    .container {
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 296px;
    }
    .logo-footer {
        cursor: pointer;
    }
    .company-introduce {
        display: flex;
        flex-direction: column;
    }
    .text-call {
        display: block;
        color: #fff;
        font-family: Inter,serif;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 22px;
    }
    .rights {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 48px;
        &-links--wrapper {
            width: 100%;
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-around;
            margin-bottom: 50px;
        }
        &-link {
            display: flex;
            flex-direction: column;
            margin-top: 20px;
        }
        &-link a {
            display: block;
            color: #02c076;
            font-family: Inter, serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: 20px;
        }
    }
    .copyright {
        color: rgba(255, 255, 255, 0.38);
        text-align: center;
        font-family: Inter, serif;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 20px;
        margin-right: 4px;
    }
    .underline-term {
        width: 79px;
        height: 1px;
        background: rgba(255, 255, 255, 0.38);
    }
    .underline-policy {
        width: 91px;
        height: 1px;
        background: rgba(255, 255, 255, 0.38);
    }
    .contacts {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        margin-top: 24px;
        &-links-container {
            display: flex;
            flex-direction: column;
        }
        &-links--wrapper {
            display: flex;
            flex-direction: row;
            justify-content: space-around;
            width: 100%;
            margin-top: 42px;
        }
        &-links:first-child {
            margin-right: 40px;
        }
        &-link a {
            color: #fff;
            font-family: Inter, serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 700;
            line-height: 24px;
        }
        &-link {
            margin-top: 12px;
            text-align: center;
        }
        &-header {
            text-align: center;
            color: rgba(255, 255, 255, 0.38);
            font-family: Inter, serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: 24px;
        }
    }
    .social-networks {
        display: flex;
        flex-direction: row;
        align-items: center;
        margin-top: 16px;
    }
    .social-link {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 48px;
        height: 48px;
        border-radius: 12px;
        border: 2px solid #02c076;
        background: #02c076;
    }
    .social-link a {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .social-link:not(:last-child) {
        margin-right: 12px;
    }
    .text-call {
        text-align: center;
        margin-top: 32px;
        width: 100%;
    }
}
  @media screen and (min-width: 1200px) {
      .mob {
          display: none;
      }
      .desk {
          display: flex;
          height: 320px;
          padding-top: 48px;
      }
      .container {
          width: 1080px;
          margin: 0 auto;
          align-items: start;
      }
      .useful-information {
          display: flex;
          flex-direction: row;
      }
      .rights {
          display: flex;
          flex-direction: row;
          align-items: center;
          margin-top: 40px;
      }
      .rights-link {
          margin-left: 28px;
          margin-top: 0;
      }
      .contacts {
          flex-direction: row;
          align-items: start;
          margin-left: 88px;
          &-links-container {
              display: flex;
              flex-direction: column;
              align-items: start;
              width: 120px;
          }
          &-link {
              text-align: start;
          }
          &-links-container:not(:last-child) {
              margin-right: 48px;
          }
      }
      .social-link {
          width: 40px;
          height: 40px;
          border-radius: 8px;
      }
      .social-link:not(:last-child) {
          margin-right: 8px;
      }
      .copyright {
          margin-right: 0;
      }
      .text-call {
          text-align: start;
          margin-top: 32px;
          width: 400px;
          height: 60px;
      }
  }
</style>
