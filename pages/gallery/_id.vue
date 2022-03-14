<template>
  <div class="imageGallery">
    <nuxt-link to="/gallery">
      Retour
    </nuxt-link>
    <div class="lightbox">
      <nuxt-img :src="`/images/img${id}.jpg`" />
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      id: this.$route.params.id
    }
  }
}
</script>

<style>
.imageGallery{
  position: absolute;
  top:0; right:0; left:0;
  max-width:900px;
  min-height: 100vh;
  background-color: rgba(0,0,0,0.9);
  z-index: 100;
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.imageGallery a {
  padding: 20px;
  color: #f1f1f1;
  text-decoration: none;
  transition: .2s;
}
.imageGallery a:hover{
  color: #999;
}
.lightbox{
  width:100%;
}
.lightbox img{
  width:100%;
}
</style>
