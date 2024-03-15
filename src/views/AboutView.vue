<template>
  <main>
    <div class="about-content">
      <h1>{{ page.title }}</h1>
      <p class="sub-title">{{ page.subTitle }}</p>
      <p>{{ page.text1 }}</p>
      <p>{{ page.text2 }}</p>
    </div>
    <BorderedImage src="../../public/assets/images/a.jpeg"/>
  </main>
</template>

<script>
import BorderedImage from "@/components/BorderedImage.vue";

export default {
  components: {
    BorderedImage
  },
  data() {
    return {
      page: {
        "title": "About us",
        "subTitle": "Subheading for description or instructions",
        "text1": "Body text for your whole article or post. We’ll put in some lorem ipsum to show how a filled-out page might look:",
        "text2": "Excepteur efficient emerging, minim veniam anim aute carefully curated Ginza conversation exquisite perfect nostrud nisi intricate Content. Qui  international first-class nulla ut. Punctual adipisicing, essential lovely queen tempor eiusmod irure. Exclusive izakaya charming Scandinavian impeccable aute quality of life soft power pariatur Melbourne occaecat discerning. Qui wardrobe aliquip, et Porter destination Toto remarkable officia Helsinki excepteur Basset hound. Zürich sleepy perfect consectetur."
      }
    }
  }
};
</script>

<style scoped>
  main {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 4rem;
  }

  .about-content {
    margin-top: 4rem;
  }

  h1 {
    margin-bottom: 3rem;
  }

  .sub-title {
    margin-bottom: 2rem;
  }

  p {
    font-size: 20px;
  }

  p:nth-of-type(2) {
    margin-bottom: 1rem;
  }
</style>
