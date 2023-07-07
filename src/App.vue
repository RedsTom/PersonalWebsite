<script setup lang="ts">
import Landing from './components/sections/Landing.vue';
import Navbar from './components/sections/Navbar.vue';
import Separator from './components/global/Separator.vue';
import Projects from './components/sections/Projects.vue';
import Links from './components/sections/Links.vue';
import Stack from './components/sections/Stack.vue';
import Contact from './components/sections/Contact.vue';

import sign from './assets/signature.png';
</script>

<template>
  <Navbar/>

  <div class="content">
    <Landing/>

    <div class="content">
      <div class="grid f">
        <div class="projects">
          <Projects/>
        </div>
        <div class="contact">
          <Contact/>
        </div>
      </div>
      <div class="grid s">
        <div class="links">
          <Links/>
        </div>
        <div class="stack">
          <Stack/>
        </div>
      </div>
    </div>

    <footer>
        <img :src="sign" alt="sign" id="sign" draggable="false" />
    </footer>
  </div>
</template>

<style scoped lang="scss">
.content {
  padding: 2rem;

  @media screen and (max-width: 500px) {
    padding: 2rem .5rem;
  }
}

footer {
  text-align: center;

  padding: 0 3rem;
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

#sign {
  height: 10rem;
}
</style>
