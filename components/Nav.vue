<template>
  <nav>
    <div class="navBar">
      <nuxt-link to="/">
        <h2>{{ titreMenu }}</h2>
      </nuxt-link>
      <span>|</span>
      <nuxt-link to="/gallery">
        <h2>{{ page }}</h2>
      </nuxt-link>
      <span>|</span>
      <nuxt-link to="/video">
        <h2>{{ video }}</h2>
      </nuxt-link>
      <span>|</span>
      <nuxt-link to="/newsletters">
        <h2>{{ page1 }}</h2>
      </nuxt-link>
    </div>
  </nav>
</template>

<script>

export default {
  name: 'Nav',
  data () {
    return {
      titreMenu: 'Actualités',
      page: 'Galerie',
      page1: 'Newsletter',
      info: 'Infos parents',
      video: 'Videos'
    }
  }
}
</script>

<style scoped>
nav{
  position:fixed;
  top:90px;
  width:100%;
  max-width:900px;
  height:40px;
  z-index:2;
  background-color:#333;
  margin-bottom: 20px;
}
nav .navBar{
  display:flex;
  align-items: center;
  max-width:100%;
  height:40px;
  padding: 0 10px;
}
nav h2, nav span{
  font-size:14px;
  font-weight: normal;
  padding: 0 5px;
  color: #f1f1f1;
  text-align: center;
}
nav a{
  text-decoration: none;
}
</style>
