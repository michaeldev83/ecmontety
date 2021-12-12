<template>
  <div class="mainVideo">
    <h2>2021</h2>
    <section class="video">
      <div>
        <div v-for="(video,index) in videos.annee2021" :key="index">
          <h3>{{ video.name }}</h3>
          <div class="lecteur">
            <div class="panel" v-for="(vid, index) in video.video" :key="index">
              <iframe
                width="560"
                height="315"
                :src="vid.url"
                :title="vid.name"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              />
            </div>
          </div>
          <hr>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import videos from '@/video.json'

export default {
  name: 'Video',
  data () {
    return {
      videos
    }
  }
}
</script>
<style scoped>
.mainVideo {
  position:relative;
  top:140px;
  width:100%;
  overflow: hidden;
  padding: 10px;
  max-width: 80rem;
  margin: 0 auto;
}
.mainVideo h2 {
  text-align: center;
  padding: 10px 20px 20px;
}
.video h3 {
  padding: 10px 0 0;
  text-align: center;
}
.lecteur {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  justify-content: center;
  align-items: center;
  grid-gap: 10px;
  padding-top: 20px;
}
.lecteur iframe {
  box-shadow: 0px 0px 2px 2px rgba(0,0,0,0.2);
  border-radius: 10px;
  margin-bottom: 10px;
  margin: 0 auto;
  width: 100%;
}
.lecteur .panel{
  width: 100%;
  height: auto;
  object-fit: cover;
}
.video hr {
  border: none;
  background-color: #dadada;
  height:1px;
  width: 50%;
  margin: 20px auto;
}
</style>
