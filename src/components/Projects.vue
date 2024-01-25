<template>
    <div class="container">
      <div v-for="(card, index) in cards" :key="index" class="card">
        <img :src="card.image" alt="Card Image" class="card-image">
        <p class="description">{{ card.description }}</p>
      </div>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const cards = ref([
        { image: 'src/assets/images/z.png', description: 'Description 1' },
        { image: 'src/assets/images/z.png', description: 'Description 2' },
        { image: 'src/assets/images/z.png', description: 'Description 3' },
        { image: 'src/assets/images/z.png', description: 'Description 4' }
      ]);
  
      return { cards };
    },
  };
  </script>
  
  <style lang="scss" scoped>
@import "../assets/scss/variables";
  .container {
    display: flex;
    align-items: center;
    justify-content: center;

    color: $light;
    background-color: $dark;
  }
  .card {
    border: 1px solid #ccc;
    padding: 10px;
    margin: 10px;
    text-align: center;
  
    .card-image {
      width: 100%;
      max-height: 200px; // Adjust as needed
      object-fit: cover;
    }
  
    .description {
      margin-top: 10px;
    }
  }
  </style>
  