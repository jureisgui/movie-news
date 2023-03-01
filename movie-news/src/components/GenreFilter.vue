<template>
    <!-- <h1>Filter news by genre</h1>
    <div class="genre-container">
        <div v-for="genres in movie_genres" class="genre" @click="search_query=genres;news_fetch();">
            <img :src="genres.img" alt="">
            <h3>{{genres.genre}}</h3>   
        </div>
    </div> -->


    <!-- <div class="genre-container">
        <div class="genre horror">
            <img src="../assets/images/horror.png" alt="">
            <h3>Horror</h3>
        </div>
        <div class="genre scifi">
            <img src="../assets/images/scifi.png" alt="">
            <h3>Sci-fi</h3>
        </div>
        <div class="genre fantasy">
            <img src="../assets/images/fantasy.png" alt="">
            <h3>Fantasy</h3>
        </div>
        <div class="genre comedy">
            <img src="../assets/images/comedy.png" alt="">
            <h3>Comedy</h3>
        </div>
        <div class="genre drama">
            <img src="../assets/images/drama.png" alt="">
            <h3>Drama</h3>
        </div>
        <div class="genre adventure">
            <img src="../assets/images/adventure.png" alt="">
            <h3>Adventure</h3>
        </div>
        <div class="genre action">
            <img src="../assets/images/action.png" alt="">
            <h3>Action</h3>
        </div>
        <div class="genre mystery">
            <img src="../assets/images/mystery.png" alt="">
            <h3>Mystery</h3>
        </div>
        <div class="genre historical">
            <img src="../assets/images/historical.png" alt="">
            <h3>Historical</h3>
        </div>
        <div class="genre animation">
            <img src="../assets/images/animation.png" alt="">
            <h3>Animation</h3>
        </div>
        <div class="genre romance">
            <img src="../assets/images/romance.png" alt="">
            <h3>Romance</h3>
        </div>
    </div> -->
    
</template>

<style scoped>
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

// <script>
// export default {
//   data(){ //data start
//     return{
//       movie_genres:[
//         {
//           genre:"Horror",
//           img:"./assets/images/horror.png"
//         },
//         {
//           genre:"Sci-fi",
//           img:"./assets/images/scifi.png"
//         },
//         {
//           genre:"Fantasy",
//           img:"./assets/images/fantasy.png"
//         },
//         {
//           genre:"Comedy",
//           img:"./assets/images/comedy.png"
//         },
//         {
//           genre:"Drama",
//           img:"./assets/images/drama.png"
//         },
//         {
//           genre:"Adventure",
//           img:"./assets/images/adventure.png"
//         },
//         {
//           genre:"Action",
//           img:"./assets/images/action.png"
//         },
//         {
//           genre:"Mystery",
//           img:"./assets/images/mystery.png"
//         },
//         {
//           genre:"Historical",
//           img:"./assets/images/mystery.png"
//         },
//         {
//           genre:"Animation",
//           img:"./assets/images/animation.png"
//         },
//         {
//           genre:"Romance",
//           img:"./assets/images/romance.png"
//         }    
//       ],
//       search_query:''
          
//   } //data end  
// }}
// </script>


<script setup>
import Home from "../App.vue";



</script>


