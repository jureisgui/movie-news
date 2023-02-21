<template>
    <h1>Filter news by genre</h1>
    <div class="genre-container">
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
    </div>

    
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
    }

    .genre img{
        max-width: 50px;
    }

    h3{
        margin: 0;
    }  
</style>


