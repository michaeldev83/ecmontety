<template>
  <div class="main">
    <div class="body">
      <h2>championnats Pré Excellence / Honneur</h2>
      <div class="items">
        <img src="@/static/logoEquipes/claretMontety.jpeg" alt="">
        <nuxt-link to="/championnat1">Equipe1</nuxt-link>
      </div>
      <div class="items">
        <img src="@/static/logoEquipes/claretMontety.jpeg" alt="">
        <nuxt-link to="/championnat2">Equipe2</nuxt-link>
      </div>
    </div>
  </div>
</template>
<style scoped>
.body{
  position:relative;
  top:140px;
  width:100%;
  overflow: hidden;
  padding:10px 0px 30px;
  margin-bottom: 10px;
  text-align: center;
}
.items {
  max-width: 200px;
  margin: 10px auto;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 0 2px 2px rgba(0,0,0,0.2);
  border-radius: 10px;
  padding: 10px;
}
.items img {
  width: 50px;
  padding-right: 20px;
}
.items a {
  text-decoration: none;
  color:#333;
}
</style>
