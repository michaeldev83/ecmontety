<template>
  <nav>
    <div class="navBar">
      <nuxt-link to="/">
        <h2>{{ titreMenu }}</h2>
      </nuxt-link>
      <span>|</span>
      <div class="dropdown">
        <h2>{{ championnat }}</h2>
        <ul>
          <li>
            <nuxt-link to="/championnat1">
              Equipe1
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/championnat2">
              Equipe2
            </nuxt-link>
          </li>
        </ul>
      </div>
      <span>|</span>
      <nuxt-link to="/gallery">
        <h2>{{ page }}</h2>
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
      video: 'Videos',
      championnat: 'Championnats'
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
.dropdown {
  position: relative;
  width: 100px;
}

.dropdown ul{
  display: none;
  background-color: #333;
  color: #fff;
  padding: 0 10px;
}
.dropdown li{
  list-style-type: none;
  padding-bottom: 5px;
}
.dropdown li a {
  text-decoration: none;
  color: #fff;
}
 .dropdown li a:hover {
  color: #999;
  transition: 0.2s ease-in-out;
}
.dropdown:hover {
  top:29px;
}
.dropdown:hover > h2 {
  padding-bottom: 10px;
}
.dropdown:hover > ul {
  display: block;
}

</style>
