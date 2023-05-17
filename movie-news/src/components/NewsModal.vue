<template>
    <div class="modal-bg">
        <div class="news-container">
          <button class="close-button" @click="closeModal">x</button>
          <div class="thumbnail-container">
              <img :src="modal_prop.urlToImage" alt="" class="thumbnail">
          </div>
          <div class="text-container">
              <h2>{{ modal_prop.title }}</h2>
              <h3>Author: {{ modal_prop.author }}</h3>
              <h3>Date: {{ modal_prop.publishedAt }}</h3>
              <p>{{ modal_prop.content }}</p>
              <a :href="modal_prop.url" target="_blank">Visit source to read full article</a> 
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
  z-index: 100;
}

.news-container{
  border: 1px solid #f2f2f2;
  border-radius: 6px;
  padding: 0.3em 1.5em;
  margin: 1em;
  background-color: #1D1A48;
  position: relative;
}

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

a{
  color:#f2f2f2;
}

.close-button {
  position: absolute;
  top: 0.5rem;
  right: 0.5rem;
  background: none;
  border: none;
  font-size: 1.5rem;
  color: #999;
  cursor: pointer;
}
</style>

<script setup>
import { ref } from 'vue';

const closeModal = () => {
  // Emit an event or perform necessary actions to close the modal
  // For example, you can use a ref to control the modal's visibility
  const modalVisible = ref(true);
  modalVisible.value = false;
};

  defineProps({
      modal_prop:{
      type: Object,
      required: true
      }
      });
</script>