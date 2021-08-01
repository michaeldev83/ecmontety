<template>
  <div class="mainGallery">
    <h2>2021</h2>
    <div class="gallery">
      <div v-for="photo in photos.annee2021" :key="photo.id" class="gallery-panel">
        <router-link v-if="photo.tag === 2021" :to="{path: `/gallery/${photo.id}`}">
          <img :src="thumbUrl(photo.filename)">
        </router-link>
      </div>
    </div>
    <h2>Avant</h2>
    <div class="gallery">
      <div v-for="photo in photos.annee2020" :key="photo.id" class="gallery-panel">
        <div v-if="photo.tag === 2020">
          <router-link :to="`/gallery/${photo.id}`">
            <img :src="thumbUrl(photo.filename)">
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
  },
  methods: {
    thumbUrl (filename) {
      return require(`@/assets/thumbnails/${filename}.jpg`)
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
.mainGallery h2{
  text-align: center;
  padding: 10px 20px 20px;
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
