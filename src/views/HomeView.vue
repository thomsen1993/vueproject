<script setup>
import Btn from "@/components/Btn.vue";
</script>

<template>
  <main>
    <div class="title">
      <h1>Home Page Title</h1>
      <p>And a subheading describing the web site</p>
      <Btn></Btn>
    </div>
    <article>
      <div>
        <BorderedImage :imageSrc="'@/assets/hero.avif'" />
      </div>
    </article>
  </main>
</template>
<script>
import BorderedImage from "@/components/BorderedImage.vue";

export default {
  components: {
    BorderedImage,
  },
};
</script>

<style scoped>
.title {
  text-align: center;
}
</style>
