<template>
    <div class="modal-bg">
        <div class="news-container">
            <div class="thumbnail-container">
                <img :src="modal_news_obj.urlToImage" alt="" class="thumbnail">
            </div>
            <div class="text-container">
                <h2>{{ modal_prop.title }}</h2>
                <h3>{{ modal_news_obj.author }}</h3>
                <h3>{{ modal_news_obj.source}}</h3>
                <h3>{{ modal_news_obj.publishedAt }}</h3>
                <p>{{ modal_news_obj.content }}</p>
                <a :href="modal_news_obj.url">Visit source</a> 
            </div>
        </div>
    </div>    
</template>

<style scoped>

.modal-bg{
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, 0.3);
    display: flex;
    justify-content: center;
    align-items: center;
}
.news-container{
  border: 1px solid #f2f2f2;
  border-radius: 6px;
  padding: 0.3em 1.5em;
  margin: 1em;
  background-color: #1D1A48;
}

/* .text-container{
  text-align: center; 
} */

.thumbnail-container{
  text-align: center;
  padding-top: 1em;
}

.thumbnail{
  width: 300px;
  object-fit: cover;
  border-radius: 6px;
  filter: drop-shadow(6px 0 6px #8C0343);
}

h2{
  text-decoration: underline;
}
</style>

<script>

</script>

<script setup>
import NewsArticle from './NewsArticle.vue'
</script>