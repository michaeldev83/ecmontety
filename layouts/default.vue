<template>
  <div class="container">
    <header-top />
    <nav-top />
    <Nuxt />
    <footer-bottom />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Nav from '@/components/Nav.vue'
import Footer from '@/components/Footer.vue'

export default {
  components: {
    'nav-top': Nav,
    'header-top': Header,
    'footer-bottom': Footer
  }
}
</script>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding:0;
}
body{
  margin: 0 auto;
  max-width: 900px;
}
.container{
  position: relative;
  width: 100%;
  margin: 0 auto;
}
.block{
  display: block!important;
}
p img{
  max-width: 100%;
  height: auto;
}
</style>
