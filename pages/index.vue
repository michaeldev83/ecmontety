<template>
  <div class="main">
    <article v-for="article in articles" :key="article.id">
      <div class="image">
        <img :src="article.img" :alt="article.alt">
      </div>
      <h2>{{ article.title }}</h2>
      <span>{{ article.date }}</span>
      <nuxt-content :document="article" />
    </article>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const articles = await $content('articles')
      .sortBy('id', 'desc')
      .fetch()
    return {
      articles
    }
  }
}
</script>

<style>
.main{
  padding: 0 5px;
}
article{
    position:relative;
    top:140px;
    width:100%;
    overflow: hidden;
    padding:10px 10px 30px;
    box-shadow: 0px 0px 2px 2px rgba(0,0,0,0.2);
    border-radius: 10px;
    margin-bottom: 10px;
}
article h2{
    padding: 10px 0 0 0;
}
article .image{
    text-align: center;
    max-width: 600px;
    margin: 10px auto;
    box-shadow: 0 0 2px 2px rgba(0,0,0,0.3);
    border-radius:7px;
    padding:5px 5px 0;
}
article .image img{
    max-width:100%;
    height: auto;
    border-radius:7px;
    background-size: cover;
}
article span{
    font-size:12px;
    color:#333;
}
article hr{
    border: none;
    background-color: #dadada;
    height:1px;
    width: 50%;
    margin: 20px auto;
}
article ul{
  padding-left: 30px;
}
/* Document Markdown */
.nuxt-content{
  padding-top:20px;
}
.nuxt-content h3{
  padding: 10px 0;
}
.nuxt-content p{
  padding: 10px 5px;
}

</style>
