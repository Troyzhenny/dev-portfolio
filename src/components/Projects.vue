<template>
  <div class="project--container" id="projects">
    <div class="heading--cont">
      <h2>SELECTED WORK.</h2>
    </div>
    <div class="row">
      <a v-for="(card, index) in cards" :key="index" :href="card.url" target="_blank" class="card">
        <img :src="card.image" alt="Card Image" class="card-image">
        <span>
          <h3 class="title">{{ card.title }} <i class="fa-solid fa-arrow-right"></i></h3>
        </span>
        <p class="description">{{ card.description }}</p>
        <br>
        <div>
          <a :href="card.source" target="_blank" @click="handleSourceLink(card.source)">
            <button type="button">
              {{ card.source === '' ? 'Private' : 'Source' }}
              <i class="fa-solid fa-code"></i>
            </button>
          </a>
        </div>
      </a>
    </div>
  </div>
</template>
  
<script>
import { ref } from 'vue';

export default {
  setup() {


    // Arry of images with project information
    const cards = ref([
      {
        title: "expensetracker.app",
        image: "/images/soon.svg",
        description: "lorem Ipsum Is my bestest friend in the entire world.",
        url: "https://www.codewars.com/dashboard",
        source: "https://www.codewars.com/dashboard",
      },
      {
        title: "dominospos.app",
        image: "/images/soon.svg",
        description: "lorem Ipsum Is my bestest friend in the entire world.",
        url: "https://www.codewars.com/dashboard",
        source: "https://www.codewars.com/dashboard",
      },
      {
        title: "kyromerch.shop",
        image: "/images/soon.svg",
        description: "lorem Ipsum Is my bestest friend in the entire world.",
        url: "https://www.codewars.com/dashboard",
        source: "",
      },
      {
        title: "playstationclone.xyz",
        image: "/images/soon.svg",
        description: "lorem Ipsum Is my bestest friend in the entire world.",
        url: "https://www.codewars.com/dashboard",
        source: "https://github.com/Troyzhenny/playstation.com-clone",
      },
      {
        title: "tevintc.xyz",
        image: "/images/devp.svg",
        description: "Version 2 of my first portfolio created with vuejs.",
        url: "https://www.patreon.com/Troyzhen?fan_landing=true&view_as=public",
        source: "https://github.com/Troyzhenny/dev-portfolio",
      },
      {
        title: "pbrp.site",
        image: "/images/soon.svg",
        description: "A website I created for the pbrp ragemp GTA V server",
        url: "https://www.codewars.com/dashboard",
        source: "",
      },
    ]);

    const handleSourceLink = (source) => {
      if (source === "") {
        alert("Sorry, but this source is private.");
      }
    };

    return { cards, handleSourceLink };
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
    margin-top: 50px;
    width: 100%;
    height: 100%;

    i {
      font-size: .70em;
      transform: rotateZ(-45deg);
    }

    button {
      width: 8rem;
      height: 2.5rem;
      border-radius: 5px;
      border: 1px solid $lightGray;
      background-color: $darkGray;
      color: $light;
      font-size: 1em;
      margin: 1.5rem;
      cursor: pointer;
    }
  }
}

.card {
  display: flex;
  flex-direction: column;
  place-items: center;
  text-align: center;
  border-radius: 5px;
  box-shadow: 10px 10px 20px 0px $projectCardShadow;
  width: 500px;
  height: 100%;
  margin: 50px;


  .card-image {
    width: 100%;
    max-height: 300px;
    object-fit: cover;
    border-radius: 5px 5px 0 0;
  }

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

    .description {
      color: $light;
    }
  }


  .title {
    font-weight: 600;
    font-size: 1.5em;
    margin: 1rem;
  }

  .description {
    margin-top: 20px;
    padding: 0 20px;
    font-size: 1em;
    text-align: left;
    color: $lightGray;
  }
}

// Queries //
/* Styles for smaller screens */
@media screen and (max-width: 768px) {
  .project--container {
    .heading--cont>h2 {
      font-size: 2.8em;
      line-height: 1.1;
      margin: 50px 0 -40px 50px;
    }

    .title {
      color: $mainColor;
      font-weight: 600;
      font-size: 1.5em;
      margin: 2rem 0 0 0;
    }

    .description {
      padding: 0 .8rem;
      font-size: 1em;
      text-align: left;
    }
  }
}
</style>
  