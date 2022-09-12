<script setup lang="ts">
import Spanize from "../global/Spanize.vue";
</script>

<template>
  <div class="navbar">
    <div class="logo">
      <h2>
        <Spanize text="|tom butin|" />
      </h2>
    </div>
  </div>
</template>

<style lang="scss">
.navbar {
  display: flex;
  align-items: center;
  justify-content: center;

  height: 4rem;
}
.navbar .logo {
  width: fit-content;

  display: flex;
  flex-direction: column;


  h2 {
    height: 1rem;
    width: 225px;

    display: flex;
    justify-content: space-between;

    & > * {
      &:first-of-type, &:last-of-type {
        color: var(--primary-text);
      }
    }
  }
}
</style>
