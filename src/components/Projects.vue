<template>
  <div class="container">
      <div class="heading--cont">
        <h2>SELECTED PROJECTS</h2>
      </div>
      <div class="row">
        <div v-for="(card, index) in cards" :key="index" class="card">
          <img :src="card.image" alt="Card Image" class="card-image">
          <h3 class="title">{{ card.title }} <i class="fa-solid fa-arrow-right"></i></h3>
          <p class="description">{{ card.description }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const cards = ref([
        { title: 'tevintc.xyz', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' },
        { title: 'playstationclone.xyz', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' },
        { title: 'kyromerch.shop', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' },
        { title: 'dominospos.app', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' },
        { title: 'expensetracker.app', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' },
        { title: 'pbrp.site', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' }
      ]);
  
      return { cards };
    },
  };
  </script>
  
  <style lang="scss" scoped>
@import "../assets/scss/variables";
  .container {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    min-height: 100vh;

    color: $light;
    background-color: $dark;

    .heading--cont {
      display: flex;
      width: 100%;
    
      h2 {
        font-size: 5em;
        margin: 60px;
      }
    }

    .row {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      width: 100%;
      height: auto;
      margin-top: 50px;

      i {
        font-size: .70em;
        transform: rotateZ(-45deg);
      }
    }
  }
  .card {
    border: 1px solid #ccc;
    border-radius: 5px;
    width: 500px;
    height: 500px;
    padding: 90px;
    margin: 50px;
    text-align: center;
  
    .card-image {
      width: 100%;
      max-height: 200px;
      object-fit: cover;
    }

    .title {
     font-weight: 600;
     font-size: 1.5em;
    }
  
    .description {
      margin-top: 10px;
    }
  }
  </style>
  