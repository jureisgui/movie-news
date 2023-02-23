<template>
    
    <NewsModal
    :news_article='modal_news_obj'
    @click='modal_on=false'
    v-if='modal_on' />

    <NewsArticle
    v-for='(news,ind) in news_articles_array'
    :news_article='news'
    :key='ind'
    @click='modal_news_obj=news;modal_on=true' />

    
</template>

<script>
export default {
  data(){ //data start
    return{
      modal_news_obj:{
        source:{id:'',name:''},
        author:'',
        title:'',
        description:'',
        url:'',
        urlToImage:'',
        publishedAt:'',
        content:''
      },
      modal_on:false
    }    
  }
}
</script>


<script setup>

import NewsModal from './NewsModal.vue';
import NewsArticle from './NewsArticle.vue';


</script>