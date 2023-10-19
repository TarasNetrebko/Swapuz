
<template>
  <MainLayout>
    <template #content>
        <div class="container">
          <div class="hero--wrapper">
              <h1 class="hero-title"></h1>
              <p class="hero-subtitle"></p>
              <div class="hero-links">
                  <a href="" class="hero-links-trust-pilot"></a>
                  <div class="hero-links-download">
                      <a href="" class="hero-links-download-google-play"></a>
                      <a href="" class="hero-links-download-app-store"></a>
                  </div>
              </div>
          </div>
            <div class="exchange--wrapper">
                <div class="exchange-header">
                    <h2 class="exchange-title"></h2>
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
                <div class="exchange-get">
                    <input type="number" class="exchange-get-input">
                    <div class="exchange-send-currency"></div>
                </div>
                <button type="submit">Exchange now</button>
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

<style>
@media screen and (min-width: 1200px) {
    .container {
        margin: 0 auto;
        padding: 88px 0 120px 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 1080px;
    }
}
</style>

