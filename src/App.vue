<script setup>
import { RouterLink, RouterView } from "vue-router";
import Btn from "./components/Btn.vue";
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="100"
      height="100"
    />

    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink>
      <Btn></Btn>
    </nav>
  </header>

  <RouterView />

  <footer>FOOTER</footer>
</template>

<style scoped>

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

nav a.router-link-exact-active {
  text-decoration: underline;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  color: black;
}
</style>
