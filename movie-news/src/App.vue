<script setup>
import Header from './components/Header.vue'
// import Search from './components/Search.vue';
import NewsArticle from './components/NewsArticle.vue'
import GenreFilter from './components/GenreFilter.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

</script>

<template>
  <div>
    <Header class="infront"/>

    <div class="welcome">
      <p>Welcome!</p>
      <p>Here you will find the latest news about the movies you want to watch.</p>
    </div>

    <h1>Search for specific news</h1>
    <div class="search-section">
        <input type="text" class="search-input" v-model="search_query" placeholder="Enter movie topic">
        <span class="search-button" @click="news_fetch" :class="{noClick:!search_query.length}"><img class="search-icon" src="./assets/images/search.png" alt=""></span>
    </div>

    <h1>Filter news by genre</h1>

    <div class="genre-container">
    
        <div v-for="genres in movie_genres" class="genre" @click="search_query=genres;news_fetch();">
            <img :src="genres.img" alt="">
            <h3>{{genres.genre}}</h3>   
        </div>
    </div>

    <!-- <GenreFilter/> -->

    <h1>Latest News</h1>

    <Main :news_articles_array='news_array' />
    <!-- <NewsArticle v-for="news in news_array" :news_article="news"  /> -->

    <Footer />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Varela+Round&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Varela&display=swap');

.welcome{
    text-align: center;
    padding: 1em;
    padding-bottom: 0;
  }

  /* .infront{
    z-index: 99;
  } */

  .search-section{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    
  }

  .search-input{
    font-family: 'Varela', sans-serif;
    font-size: 16px;
    border-radius: 6px;
  }

  .search-button{
      text-align: center;
      /* pointer-events: none; */
      background-color: #8C0343;
      border-radius: 50%;
      max-width: 30px;
      max-height: 30px;
  }

  .search-icon{
    max-width: 20px;
    max-height: 20px;
    padding: 0.3em;
  } 
  
  .genre{
        border: 1px solid #f2f2f2;
        border-radius: 6px;
        padding: 0.3em 1.5em;
        margin: 0.5em;
        text-align: center;
        max-width: 70px;
    }

    .genre-container{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        margin: 0.5em;
        /* padding-bottom: 1em ; */
    }

    .genre img{
        max-width: 50px;
    }

    h3{
        margin: 0;
    }  

</style>

<script>
export default {
  data(){ //data start
    return{
      news_array:[],
      movie_genres:[
        {
          genre:"Horror",
          img:"https://i.ibb.co/FqSHDB4/horror.png"
        },
        {
          genre:"Sci-fi",
          img:"https://i.ibb.co/hMFTCrG/scifi.png"
        },
        {
          genre:"Fantasy",
          img:"https://i.ibb.co/Vt2Dssp/fantasy.png"
        },
        {
          genre:"Comedy",
          img:"https://i.ibb.co/pXWBm61/comedy.png"
        },
        {
          genre:"Drama",
          img:"https://i.ibb.co/CKD5G2R/drama.png"
        },
        {
          genre:"Adventure",
          img:"https://i.ibb.co/vkW6dTh/adventure.png"
        },
        {
          genre:"Action",
          img:"https://i.ibb.co/0Bc9YCQ/action.png"
        },
        {
          genre:"Mystery",
          img:"https://i.ibb.co/3hRdf2D/mystery.png"
        },
        {
          genre:"Historical",
          img:"https://i.ibb.co/dPWs3ds/historical.png"
        },
        {
          genre:"Animation",
          img:"https://i.ibb.co/6t2tM8X/animation.png"
        },
        {
          genre:"Romance",
          img:"https://i.ibb.co/p4943HT/romance.png"
        }    
      ],
      search_query:''
          
  } //data end  
},

methods:{
  async news_fetch(){
    const response = await fetch('https://newsapi.org/v2/everything?q="'+this.search_query+' movies"'+'&apiKey=4d85dee1eea24f48abac2151c9f4196a');
    const received_news = await response.json();
    this.news_array = received_news.articles;

  }
}, // methods end

created(){
  this.news_fetch();
}
}
</script>
