<script setup>
import { RouterLink, RouterView } from "vue-router";
import Btn from "./components/Btn.vue";
import '@fortawesome/fontawesome-free/css/all.css'
</script>

<template>
  <header>
    <img alt="Vue logo" src="@/assets/logo.svg" width="100" height="100" />

    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink>
      <Btn></Btn>
    </nav>
  </header>

  <RouterView />

  <footer>
    <div class="socials-group">
      <img alt="Vue logo" src="@/assets/logo.svg" width="50" height="50" />
      <div class="socials">
        <a href=""><i class="fa-brands fa-facebook"></i></a>
        <a href=""><i class="fa-brands fa-instagram"></i></a>
        <a href=""><i class="fa-brands fa-linkedin"></i></a>
        <a href=""><i class="fa-brands fa-youtube"></i></a>
      </div>
    </div>
    <div class="links">
      <ul v-for="(link, index) in links" :key="index">
        <li>
          <h4>{{ link.title }}</h4>
        </li>
        <li v-for="(subLink, indexx) in link.name" :key="indexx"><a href="">{{ subLink.link1 }}</a></li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          "title": "Topic",
          "name": [
            {
              "link1": "page"
            },
            {
              "link1": "page"
            },
            {
              "link1": "page"
            },
          ]
        },
        {
          "title": "Topic",
          "name": [
            {
              "link1": "page1"
            },
            {
              "link1": "page1"
            },
            {
              "link1": "page1"
            },
          ]
        },
        {
          "title": "Topic",
          "name": [
            {
              "link1": "page2"
            },
            {
              "link1": "page2"
            },
            {
              "link1": "page2"
            },
          ]
        },
      ]
    }
  }
}
</script>

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

footer {
  display: flex;
  justify-content: space-between;
  border-top: var(--border);
  padding: 5rem 0 1rem;
  font-size: 18px;
}

.socials-group {
  display: grid;
}

.socials {
  display: flex;
  align-items: end;
  gap: 1rem;
}

.socials i {
  font-size: 24px;
  color: var(--subText);
}

.fa-brands {
  transition: .3s;
}

.fa-brands:hover {
  scale: 1.2;
}

.fa-facebook:hover {
  color: rgb(23,115,234);
}

.fa-instagram:hover {
  color: rgb(219,46,105);
}

.fa-linkedin:hover {
  color: rgb(0,115,175);
}

.fa-youtube:hover {
  color: rgb(255,0,0);
}

.links {
  display: flex;
  line-height: 2;
}

.links ul {
  border-left: var(--border);
  padding-left: 7rem;
  padding-right: 7rem;
}

.links ul:first-child {
  border: none;
}
</style>
