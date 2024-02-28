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
          <h1>I'm Tevin</h1>
          <p>
            I am a passionate web developer with a background in <br> graphic design, merging functionality with stunning
            visuals.
          </p>
          <div class="btn--container">
            <a href="#projects" class="cta--btn">
              <p>Projects</p>
            </a>
          </div>
        </div>
        <div>
        </div>

        <div class="hero--image">
          <img src="/images/progressive_app.svg" alt="hero-image">
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
@import "./assets/scss/main.scss";

.main--container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  place-items: center;
  width: 100%;
  min-height: 100vh;
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
        width: 600px;
      }
    }

    .btn--container {
      display: flex;
      gap: 30px;

      .cta--btn {
        @include cta-btn-mix;
      }
    }
  }


  .hero--text {
    h1 {
      font-family: 'Cabinet Grotesk', sans-serif;
      line-height: .8;
      color: $light;
      margin: 10px 0;
    }

    p:nth-child(1) {
      color: $mainColor;
      font-weight: 500;
    }

    p {
      font-family: 'Satoshi', sans-serif;
      color: $lightGray;
      margin: 0;
    }
  }
}

// Queries //
/* Styles for smaller screens */
@media screen and (max-width: 768px) {
  .main--container {
    .hero--text {
      margin-top: -100px;
      margin-left: 30px;
      margin-right: -50px;

      h1 {
        font-size: 4em;
      }

      p {
        font-size: 1.25em;
      }
    }

    .hero--shelf {
      .hero--image {
        display: none;
      }

      .btn--container {
        .cta--btn {
          width: 140px;
          height: 50px
        }
      }
    }
  }
}
</style>
