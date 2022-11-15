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
      <div class="grid f">
        <div class="projects">
          <Projects />
        </div>
        <div class="contact">
          <Contact />
        </div>
      </div>
      <div class="grid s">
        <div class="links">
          <Links />
        </div>
        <div class="stack">
          <Stack />
        </div>
      </div>
    </div>

    <footer>
      This website was made with ❤️ by me using Vue.js. It is hosted on Netlify.
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

.grid {
  display: grid;
  grid-gap: 1rem;

  &.f {
    grid-template-columns: 2fr 1fr;
  }

  &.s {
    grid-template-columns: 1fr 2fr;
  }

  @media screen and (max-width: 1400px) {
    display: flex;
    flex-direction: column;
  }
}
</style>
