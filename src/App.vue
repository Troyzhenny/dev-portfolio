<script setup>
import Navbar from './components/Navbar.vue';
import About from './components/About.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <header>
    <Navbar />
  </header>

  <!-- Home -- Main -->
  <main id="home">
    <div class="main--container">
      <div class="hero--shelf">
        <div class="hero--text">
          <p>Hi There!</p>
          <h2>I'm Tevin</h2>
          <p>
            I am a passionate web developer with a background in <br> graphic design, merging functionality with stunning
            visuals <br> to craft responsive and beautiful experiences for my projects.
          </p>
          <a href="#projects" class="cta--btn">
            <p>Projects</p>
          </a>
        </div>
        <div>
        </div>

        <div class="hero--image">
          <img src="./assets/images/progressive_app.svg" alt="">
        </div>
      </div>
    </div>
  </main>

  <section>
    <About />
  </section>
  
  <section>
    <Projects />
  </section>

  <section>
    <Contact />
  </section>

  <section>
    <Footer />
  </section>

</template>

<style scoped lang="scss">
@import "./assets/scss/variables";

.main--container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  width: 100%;
  min-height: 100%;
  background-color: $darkGray;

  .hero--shelf {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    min-height: 120vh;
    gap: 80px;

    .hero--image {
      img {
        width: 700px;
      }
    }


    .cta--btn {
      border: 2px solid $mainColor;
      text-decoration: none;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 3px;
      width: 180px;
      height: 50px;
      margin: 50px 0;
      
      p {
        font-family: 'Satoshi', sans-serif;
        font-size: 1.2em;
        font-weight: 500;
        color: $light;
      }

      &:hover {
        p{
          color: $secondary;
          font-weight: 800;
        }
        background-color: $mainColor;
        transform: translateY(-5px);
        transition: .5s ease;
      }


    }
  }

  .hero--text {
    h2 {
      font-family: 'Cabinet Grotesk', sans-serif;
      font-size: 5em;
      line-height: .8;
      color: $light;
      margin: 10px 0;
    }

    p {
      font-family: 'Satoshi', sans-serif;
      font-size: 1.5em;
      color: $lightGray;
      margin: 0;
    }
  }
}
</style>
