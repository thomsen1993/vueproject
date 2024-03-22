<script setup>
import Btn from "@/components/Btn.vue";
</script>

<template>
  <main>
    <div class="hero">
      <div class="title">
        <h1>Home Page Title</h1>
        <p class="sub-title">And a subheading describing the web site</p>
        <Btn></Btn>
      </div>
      <div class="hero-picture">
        <BorderedImage src="../../public/assets/images/hero.jpg" />
        <img src="../../public/assets/images/cloud.png" alt="" width="100%" class="cloud">
        <img src="../../public/assets/images/cloud.png" alt="" width="100%" class="cloud2">
      </div>
    </div>
    <section class="wrapper">
      <h2>Heading</h2>
      <p class="sub-title">Subheading to introduce testimonials</p>
      <div class="grid">
        <div class="card-container" v-for="(value, index) in card" :key="index">
          <div class="card">
            <h3>{{ value.title }}</h3>
            <div class="card-info">
              <figure>
                <img :src="value.src" alt="">
              </figure>
              <div>
                <p>{{ value.name }}</p>
                <p class="sub-text">{{ value.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

  </main>
</template>
<script>
import BorderedImage from "@/components/BorderedImage.vue";

export default {
  components: {
    BorderedImage,
  },
  data() {
    return {
      card: [
        {
          "title": "“A terrific piece of praise”",
          "name": "Jimmi",
          "description": "description",
          "src": "/public/assets/images/a.jpeg"
        },
        {
          "title": "“A fantastic bit of feedback”",
          "name": "Jimmi",
          "description": "description",
          "src": "/public/assets/images/b.jpg"
        },
        {
          "title": "“A genuinely glowing review”",
          "name": "Jimmi",
          "description": "description",
          "src": "/public/assets/images/c.jpg"
        },
      ]
    }
  }
};

</script>

<style scoped>

.hero {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  overflow: hidden;
  padding-bottom: 15rem;
  padding-top: 10rem;
}

.title {
  grid-column: 1/3;
  grid-row: 1/1;
  text-align: center;
  border: 4px double rgb(212, 212, 212);
  border-radius: 20px 0;
  background-color: rgba(0, 0, 0, .6);
  backdrop-filter: blur(5px);
  width: max-content;
  height: max-content;
  margin: 10rem auto;
  padding: 2rem;
  z-index: 1;
}

.title h1 {
  margin-bottom: 1rem;
}

.title .sub-title {
  margin-bottom: 1rem;
}

.hero-picture {
  grid-column: 1/-1;
  grid-row: 1/-1;
  position: relative;
}

.hero-picture figure {
  width: 86%;
}

.cloud {
  position: absolute;
  bottom: -15rem;
  opacity: .6;
  animation: cloud 150s infinite linear;
}

.cloud2 {
  position: absolute;
  bottom: -15rem;
  opacity: .4;
  animation: cloud2 160s infinite linear;
}

@keyframes cloud {
  from {
    left: -350px;
  }

  to {
    left: 800px;
  }
}

@keyframes cloud2 {
  from {
    left: 500px;
  }

  to {
    left: -350px;
  }
}


.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 3rem;
  margin-top: 3rem;
}

.card-container {
  position: relative;
}

.card {
  padding: 2rem;
  border-radius: 10px;
  background-color: white;
  border: var(--border);
  transition: .5s;
}

.card:hover {
  box-shadow: var(--shadow);
  transform: translate(-5px, -5px);
}

.card-container:hover::before {
  content: "";
  position: absolute;
  inset: 0%;
  transform: rotate(10deg);
  background-color: var(--bg);
  border: var(--border);
  border-radius: 10px;
  animation: rotation 1s;
  z-index: -1;
}

@keyframes rotation {
  100% {
    transform: rotate(370deg);
  }
}

.card h3 {
  margin-bottom: 3rem;
  text-align: center;
}

.card-info {
  display: flex;
  gap: 1rem;
}

.card img {
  width: 3rem;
  height: 3rem;
  object-fit: cover;
  border-radius: 100%;
}

@media screen and (max-width: 1200px) {
  .title {
    margin: 2rem auto;
  }

  .cloud, .cloud2, .cloud3 {
    width: 70%;
    bottom: -10rem;
  }
}

@media screen and (max-width: 700px) {
  .cloud, .cloud2, .cloud3 {
    display: none;
  }

  .grid {
    grid-template-columns: 1fr;
  }
}

</style>
