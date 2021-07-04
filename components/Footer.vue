<template>
  <footer>
    <div class="contact">
      <h3>Nous contacter</h3>
      <ul>
        <hr>
        <li>Dominique (Papi) - 06 00 34 34 12</li>
        <hr>
        <li>Stéphane - 06 00 34 34 12</li>
        <hr>
        <li>Enis - 06 00 34 34 12</li>
        <hr>
        <li>David - 06 00 34 34 12</li>
        <hr>
        <li>Fabien - 06 00 34 34 12</li>
        <hr>
      </ul>
    </div>
    <span>© Etoile Claret Montety | créer par Michael B</span>
  </footer>
</template>

<script>
export default {
  name: 'footer-bottom'
}
</script>

<style scoped>
footer {
  position:relative;
  top: 140px; bottom:0;
  background-color: #333;
  color: #f1f1f1;
  padding: 10px;
}
span{
    font-size:14px;
    display: block;
    text-align: center;
    padding: 20px 0;
}
.contact hr{
  border:none;
  background-color: #777;
  height:1px;
  margin: 0 auto;
  width: 100%;
}
h3{
  padding-bottom: 10px;
}
.contact li{
  padding: 7px 10px;
  list-style-type: none;
}
</style>
