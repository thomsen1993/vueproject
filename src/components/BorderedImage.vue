<template>
  <figure class="borderedImage">
      <img :src="props.src" alt="" />
  </figure>
</template>

<script setup>
const props = defineProps(['src'])
</script>

<style scoped>
.borderedImage {
  border: 2px solid var(--border);
  background-color: var(--bg);
  width: max-content;
  margin: 0 auto;
  margin-top: 4rem;
  margin-bottom: 4rem;
  transform: rotate(10deg);
  width: 100%;
  height: auto;
}

.borderedImage img {
  display: block;
  width: 100%;
  height: auto;
  transform: rotate(-10deg);
  box-shadow: var(--shadow);
}
</style>