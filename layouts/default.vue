<template>
  <div class="container">
    <header-top />
    <nav-top :titreMenu="titre" />
    <Nuxt />
    <footer-bottom />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Nav from '@/components/Nav.vue'
import Footer from '@/components/Footer.vue'

export default {
  data() {
    return {
      titre: 'Accueil et Actualités'
    }
  },
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
}
.container{
  position: relative;
  max-width: 600px;
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
