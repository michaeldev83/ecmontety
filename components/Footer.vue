<template>
  <footer>
    <div class="contact">
      <h3>Contacter nos entraineurs {{ niveau }}</h3>
      <ul>
        <hr>
        <li>Dominique (Papi) - <a href="tel:06 00 34 34 12">06 00 34 34 12</a></li>
        <hr>
        <li>Stéphane - <a href="tel:06 00 34 34 12">06 00 34 34 12</a></li>
        <hr>
        <li>Enis - <a href="tel:06 00 34 34 12">06 00 34 34 12</a></li>
        <hr>
        <li>David - <a href="tel:06 00 34 34 12">06 00 34 34 12</a></li>
        <hr>
        <li>Fabien - <a href="tel:06 00 34 34 12">06 00 34 34 12</a></li>
        <hr>
      </ul>
    </div>
    <span>© Etoile Claret Montety | créer par Michael B</span>
  </footer>
</template>

<script>
export default {
  name: 'footer-bottom',
  props: ['niveau']
}
</script>

<style scoped>
footer {
  position: relative;
  top:140px;
  bottom:0;
  left: 0;
  right:0;
  background-color: #333;
  color: #f1f1f1;
  padding: 10px;
}
footer span{
    font-size:14px;
    display: block;
    text-align: center;
    padding: 20px 0;
}
.contact a{
  text-decoration: none;
  color:#f1f1f1;
  border-bottom: 1px solid #fff;
}
.contact hr{
  border:none;
  background-color: #777;
}
.contact h3{
  padding: 10px 10px 20px;
  border-bottom: 1px solid #fff;
  text-align: center;
}
.contact ul{
  padding:10px 0;
  border-bottom: 1px solid #fff;
}
.contact li{
  padding: 7px 10px;
  list-style-type: none;
}
</style>
