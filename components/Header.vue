<template>
  <div class="header-top">
    <div class="image">
      <nuxt-img src="/imagesHeader/fond.png" alt="ballon" format="webp" sizes="sm:100vw md:50vw lg:400px" />
      <div class="club">
        <ul>
          <li>Etoile Claret Montety</li>
          <li>{{ niveau }}</li>
        </ul>
      </div>
    </div>
    <div class="logo">
      <nuxt-img src="/imagesHeader/ecmLogo2.png" alt="logo" format="webp" sizes="sm:100vw md:50vw lg:400px" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: ['niveau']
}
</script>

<style scoped>

.header-top{
  position: fixed;
  top:0;
  width: 100%;
  max-width:900px;
  margin: 0 auto;
  height:90px;
  z-index:2;
}
.image img{
  width: 100%;
  height: 90px;
}
.club{
  position: absolute;
  top:20px; right: 20px;
}
.club ul{
  display: flex;
  justify-content: center;
  align-items:center;
  flex-direction: column;
}
.club ul li{
  list-style-type: none;
  font-size: 20px;
  padding:2px 10px;
}
.club ul li:first-child{
  color:#DCC816;
}
.club ul li:last-child{
  color: #EA0C0C;
}
.logo{
  position:absolute;
  top:10px; left:5%;
  height:80px;
  width:80px;
  opacity: .8;
}
.logo img {
  width:70px;
  height:70px;
  border-radius:10px;
}
</style>
