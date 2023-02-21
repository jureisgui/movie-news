<script setup>
import Header from './components/Header.vue'
// import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <Header />
  <div class="welcome">
    <p>Welcome!</p>
    <p>Here you will find the latest news about the movies you want to watch.</p>
  </div>
  
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Varela&family=Varela+Round&display=swap');

  h1{
    font-family: 'Varela', sans-serif;
    font-size: 20px;
    color: #F2F2F2;
  }

  p{
    font-family: 'Varela Round', sans-serif;
    font-size: 16px;
    color: #F2F2F2;
  }

  h2{
    font-family: 'Varela', sans-serif;
    font-size: 16px;
    color: #F2F2F2;
  }

  h3{
    font-family: 'Varela Round', sans-serif;
    font-size: 14px;
    color: #F2F2F2;
  }

  .welcome{
    text-align: center;
    padding: 1em;
  }

</style>
