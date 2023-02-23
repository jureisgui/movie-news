<script setup>
import Header from './components/Header.vue'
// import Search from './components/Search.vue';
import NewsArticle from './components/NewsArticle.vue'
import GenreFilter from './components/GenreFilter.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

</script>

<template>

  <Header />
  <div class="welcome">
    <p>Welcome!</p>
    <p>Here you will find the latest news about the movies you want to watch.</p>
  </div>
  <!-- <Search /> -->
  <GenreFilter/>

  <h1>Latest News</h1>

  <!-- <Main :news_articles_array='news_array' /> -->
  <NewsArticle v-for="news in news_array" :news_article="news"  />

  <Footer />
  
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Varela+Round&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Varela&display=swap');

.welcome{
    text-align: center;
    padding: 1em;
    padding-bottom: 0;
  }

</style>

<script>
export default {
  data(){ //data start
    return{
      news_array:[]
          
  } //data end  
},

methods:{
  async news_fetch(){
    const response = await fetch('https://newsapi.org/v2/everything?q=movies&apiKey=4d85dee1eea24f48abac2151c9f4196a');
    const received_news = await response.json();
    // console.log(received_news);
    this.news_array = received_news.articles;

  }
}, // methods end

created(){
  this.news_fetch();
}
}
</script>
