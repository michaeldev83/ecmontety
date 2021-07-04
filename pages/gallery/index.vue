<template>
  <div class="gallery">
    <div v-for="photo in photos" :key="photo.id" class="gallery-panel">
      <router-link :to="`/gallery/${photo.id}`">
        <img :src="thumbUrl(photo.filename)">
      </router-link>
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
.gallery {
  position:relative;
  top:140px;
  width:100%;
  overflow: hidden;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  justify-content: center;
  grid-gap: 10px;
  max-width: 80rem;
  margin: 0 auto;
  padding: 10px;
}
.gallery-panel img {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 0.75rem;
}
</style>
