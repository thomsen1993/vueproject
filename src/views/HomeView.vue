<script setup>
import Btn from "@/components/Btn.vue";
</script>

<template>
  <main>
    <div class="title">
      <h1>Home Page Title</h1>
      <p class="sub-title">And a subheading describing the web site</p>
      <Btn></Btn>
    </div>
    <BorderedImage src="../../public/assets/images/hero.jpg"/>
    <section>
      <h2>Heading</h2>
      <p  class="sub-title">Subheading to introduce testimonials</p>
      <div class="grid">
        <div class="card" v-for="(value, index) in card" :key="index">
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
.title {
  text-align: center;
  margin: 5rem 0 10rem 0;
}

.title h1 {
  margin-bottom: 1rem;
}

.title .sub-title {
  margin-bottom: 1rem;
}

section {
  margin: 10rem 0;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 3rem;
  margin-top: 3rem;
}

.card {
  padding: 2rem;
  border-radius: 10px;
  box-shadow: var(--shadow);
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
</style>
