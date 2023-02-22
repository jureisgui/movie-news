<script setup>
import Header from './components/Header.vue';
import Search from './components/Search.vue';
import GenreFilter from './components/GenreFilter.vue';
import Footer from './components/Footer.vue'

</script>

<template>

  <Header />
  <div class="welcome">
    <p>Welcome!</p>
    <p>Here you will find the latest news about the movies you want to watch.</p>
  </div>
  <Search />
  <GenreFilter/>
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
