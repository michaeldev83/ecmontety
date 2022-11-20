<template>
  <div class="main">
    <div class="body">
      <u><h1>Championnat Pré Exellence</h1></u>
      <div v-for="(rencontre, index) in rencontres" :key="index" class="match">
        <h3><u>{{ rencontre.date }}</u></h3>
        <h4>{{ rencontre.lieu }}</h4>
        <div class="matchs">
          <div v-for="(match, indexMatch) in rencontre.matchs" :key="indexMatch" class="cadre">
            <div class="equipe">
              <nuxt-img :src="`/logoEquipes/${match.logo1}.jpeg`" />
              <span>{{ match.equipe1 }}</span>
            </div>
            <div class="score">
              <p v-if="match.score1 > match.score2">
                <span class="green"> {{ match.score1 }}</span> - <span> {{ match.score2 }}</span>
              </p>
              <p v-else-if="match.score2 > match.score1">
                <span> {{ match.score1 }}</span> - <span class="green"> {{ match.score2 }}</span>
              </p>
              <p v-else>
                <span> {{ match.score1 }}</span> - <span> {{ match.score2 }}</span>
              </p>
            </div>
            <div class="equipe">
              <nuxt-img :src="`/logoEquipes/${match.logo2}.jpeg`" />
              <span>{{ match.equipe2 }}</span>
            </div>
          </div>
        </div>
        <hr>
      </div>
    </div>
  </div>
</template>

<script>
import rencontres from '@/pages/championnat1/rencontres.json'

export default {
  name: 'Rencontres',
  data () {
    return {
      rencontres
    }
  }
}
</script>

<style scoped>
.main{
  padding: 0;
}
.body{
  position:relative;
  top:140px;
  width:100%;
  overflow: hidden;
  padding:10px 0px 30px;
  margin-bottom: 10px;
  text-align: center;
}
h1 { margin-bottom: 20px;}
h3 { margin: 10px auto}
h4 { margin: 0 0 20px 0}
hr {
  width: 50%;
  border: none;
  height:1px;
  background-color: #dadada;
  margin: 15px auto;
}
.green { color: rgb(24, 206, 24)}
.matchs {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
.match {
  padding: 10px;
  border-radius:10px;
  /* box-shadow: 0px 0px 2px 2px rgba(0,0,0,0.2); */
  margin: 10px;
}
.cadre{
  display: flex;
  align-items: center;
  justify-content: space-around;
  width: 100%;
  max-width: 320px;
  box-shadow: 0 0 6px 2px rgba(0,0,0,0.2);
  border-radius:10px;
  padding:10px 5px;
  margin:10px;
}
.equipe {
  display: flex;
  flex-direction: column;
  align-items: center;
  width:100px;
}
.equipe img {
  max-width:50px;
  height:50px;
  max-height: 50px;
  margin-bottom: 10px;
}
.equipe span {
  width: 100%;
  height: 50px;
}
.score {
  font-size: 25px;
  width:55px;
}

</style>
