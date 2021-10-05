<template>
  <div class="mainGallery">
    <h2>2021</h2>
    <div>
      <div v-for="(dossier, index) in photos.annee2021" :key="index">
        <h3>{{ dossier.name }}</h3>
        <div class="gallery">
          <div v-for="photo in dossier.photos" :key="photo.id" class="gallery-panel">
            <router-link :to="{path: `/gallery/${photo.id}`}">
              <nuxt-img :src="`/images/${photo.filename}.jpg`" format="webp" />
            </router-link>
          </div>
        </div>
        <hr>
      </div>
    </div>
    <h2>Années précédentes</h2>
    <div v-for="(dossier, index) in photos.annee2020" :key="index">
      <div class="gallery">
        <div v-for="photo in dossier.photos" :key="photo.id" class="gallery-panel">
          <router-link :to="{path: `/gallery/${photo.id}`}">
            <nuxt-img :src="`/images/${photo.filename}.jpg`" format="webp" />
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import photos from '@/photos.json'

export default {
  name: 'Gallery',
  data () {
    return {
      photos
    }
  }
}
</script>

<style>
.mainGallery{
  position:relative;
  top:140px;
  width:100%;
  overflow: hidden;
  padding: 10px;
  max-width: 80rem;
  margin: 0 auto;
}
.mainGallery h2, .mainGallery h3{
  text-align: center;
  padding: 10px 20px 20px;
}
.mainGallery hr {
width: 50%;
border: none;
height:1px;
background-color: #dadada;
margin: 15px auto;
}
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  justify-content: center;
  align-items: center;
  grid-gap: 10px;
}
.gallery-panel img {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 0.75rem;
}
</style>
