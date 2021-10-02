<template>
  <div class="imageGallery">
    <nuxt-link to="/gallery">
      Retour
    </nuxt-link>
    <div class="lightbox">
      <img :src="photoUrl(galerie.filename)">
    </div>
  </div>
</template>

<script>
import photos from '@/photos.json'

export default {
  data () {
    return {
      photos,
      galerie: ''
    }
  },
  created () {
    this.photo()
  },
  methods: {
    photo () {
      for (const key in this.photos) {
        for (let i = 0; i < this.photos[key].length; i++) {
          for (let p = 0; p < this.photos[key][i].photos.length; p++) {
            if (this.photos[key][i].photos[p].id === Number(this.$route.params.id)) {
              this.galerie = {
                id: this.photos[key][i].photos[p].id,
                filename: this.photos[key][i].photos[p].filename,
                tag: this.photos[key][i].photos[p].tag
              }
            }
          }
        }
      }
    },
    photoUrl (filename) {
      return require(`../../assets/images/${filename}.jpg`)
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
