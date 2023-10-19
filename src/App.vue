<script setup>
  import { RouterView } from 'vue-router'
</script>

<template>
  <RouterView />
</template>

<style lang="scss">
*,
*:before,
*:after {
  padding: 0;
  margin: 0;
  border: 0;
  box-sizing: border-box;
}
a {
  text-decoration: none;
}
ul,
ol,
li {
  list-style: none;
}
img {
  vertical-align: top;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: inherit;
  font-size: inherit;
}  body {
  height: 100%;
  line-height: 1;
  font-size: 16px;
  color: #000;
    background: #1B1A1C;
  }
  #app {
    min-height: 100%;
    overflow: hidden;
  }
</style>
