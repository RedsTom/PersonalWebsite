<script setup lang="ts">
import Landing from './components/sections/Landing.vue';
import Navbar from './components/sections/Navbar.vue';
import Separator from './components/global/Separator.vue';
import Projects from './components/sections/Projects.vue';
import Links from './components/sections/Links.vue';
import Stack from './components/sections/Stack.vue';
import Contact from './components/sections/Contact.vue';
</script>

<template>
  <Navbar />

  <div class="content">
    <Landing />

    <div class="content">
      <Projects />
      <Links />
      <Stack />
      <Contact />
    </div>

    <footer>
      This website was made with ❤️ by me using Vue.js. It is hosted on Github Pages.
    </footer>
  </div>
</template>

<style scoped lang="scss">
.content {
  padding: 2rem;
}

footer {
  text-align: center;
}
</style>