<script setup>
import { useRoute } from 'vue-router';

const route = useRoute();

console.log()
</script>

<template>
  <aside class="sidebar-menu hidden flex flex-col z-20 justify-center items-center relative">
    <nav class="menu flex flex-col m-auto text-xl">
      <RouterLink :to="{ name: 'home', hash: '#about' }" class="link py-3" :class="{'selected': route.fullPath.includes('about')}">
        <span>About</span>
      </RouterLink>
      <RouterLink :to="{ name: 'home', hash: '#experience' }" class="link py-3" :class="{'selected': route.fullPath.includes('experience')}">
        <span>Experience</span>
      </RouterLink>
      <RouterLink :to="{ name: 'home', hash: '#projects' }" class="link py-3" :class="{'selected': route.fullPath.includes('projects')}">
        <span>Projects</span>
      </RouterLink>
      <RouterLink :to="{ name: 'home', hash: '#contact' }" class="link py-3" :class="{'selected': route.fullPath.includes('contact')}">
        <span>Contact</span>
      </RouterLink>
    </nav>
    <div class="socials flex items-center justify-center space-x-5 absolute bottom-5">
        <a href="https://github.com/varsha286" target="_blank">
            <font-awesome-icon icon="fab fa-github" class="fa-xl hover:text-important" />
        </a>
        <a href="https://www.linkedin.com/in/varsha-p-37736529a/" target="_blank">
            <font-awesome-icon icon="fab fa-linkedin-in" class="fa-xl hover:text-important" />
        </a>
      </div>
  </aside>
</template>

<style scoped>
.sidebar-menu {
  width: min(75vw, 400px);
  min-height: 100vh;
  /*min-height: -webkit-fill-available;*/
  position: fixed;
  top: 0;
  right: 0;
  z-index: 6;
  background-color: #100837;
  padding: 1rem .75rem;
  /* transform: translateX(450px); */
  transition: transform .5s;
  margin: 0;
}
</style>

logo_fredchess.png
logo_fredchess.svg