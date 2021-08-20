<template>
  <footer>
    <div class="contact">
      <h3>Contacter nos entraineurs {{ niveau }}</h3>
      <ul>
        <li>Dominique (Papi) - <a href="tel:0651175205">06 51 17 52 05</a></li>
        <li>Stéphane - <a href="tel:06">06</a></li>
        <li>Enis - <a href="tel:0661671564">06 61 67 15 64</a></li>
        <li>David - <a href="tel:0675906522">06 75 90 65 22</a></li>
        <li>Fabien - <a href="tel:06">06</a></li>
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
