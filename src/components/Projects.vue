<template>
  <div class="project--container" id="projects">
    <div class="heading--cont">
      <h2>SELECTED PROJECTS</h2>
    </div>
    <div class="row">
      <a v-for="(card, index) in cards" :key="index" :href="card.url" target="_blank" class="card">
        <img :src="card.image" alt="Card Image" class="card-image">
        <span>
          <h3 class="title">{{ card.title }} <i class="fa-solid fa-arrow-right"></i></h3>
        </span>
        <p class="description">{{ card.description }}</p>
      </a>
    </div>
  </div>
</template>
  
<script>
import { ref } from 'vue';

export default {
  setup() {
    const cards = ref([
      { title: 'expensetracker.app', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.', url: 'https://www.codewars.com/dashboard'},
      { title: 'dominospos.app', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' },
      { title: 'kyromerch.shop', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' },
      { title: 'playstationclone.xyz', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' },
      { title: 'tevintc.xyz', image: 'src/assets/images/devp.svg', description: 'Version 2 of my first portfolio created with vuejs.' },
      { title: 'pbrp.site', image: 'src/assets/images/z.png', description: 'lorem Ipsum Is my bestest friend in the entire world.' }
    ]);

    return { cards };
  }
};
</script>
  
<style lang="scss" scoped>
@import "../assets/scss/variables";

.project--container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  min-height: 100vh;

  color: $light;
  background-color: $dark;

  .heading--cont {
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
  border-radius: 5px;
  box-shadow: 10px 10px 20px 0px $projectCardShadow;
  width: 500px;
  height: 500px;
  margin: 50px;
  text-align: center;

  &:hover {
    border-radius: 20px;
    transition: .2s ease-out;
    cursor: pointer;

    .card-image {
      border-radius: 20px 20px 0 0;
      transition: .2s ease-in-out;
    }

    .fa-arrow-right {
      transform: rotateZ(-45deg) translate(10px, -5px);
      transition: .3s ease;
    }

    p {
      color: $light;
    }
  }

  .card-image {
    width: 100%;
    max-height: 300px;
    object-fit: cover;
    border-radius: 5px 5px 0 0;
  }

  .title {
    font-weight: 600;
    font-size: 1.5em;
    margin: 1rem;
  }

  .description {
    margin-top: 20px;
  }
}
</style>
  