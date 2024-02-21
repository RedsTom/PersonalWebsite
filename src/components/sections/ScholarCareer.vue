<script setup lang="ts">

import Splitter from "../global/Splitter.vue";
</script>

<template>
  <Splitter>My Scholar Career</Splitter>

  <div class="content">
    <div id="experiences">
      <div class="middle-school">
        <div class="location">
          <font-awesome-icon icon="fa-solid fa-location-pin"/>
          <span>Collège Saint Joseph les Maristes</span>
        </div>
        <div class="duration">
          <font-awesome-icon icon="fa-solid fa-calendar"/>
          <span>2017 - 2021</span>
        </div>
        <div class="graduation">
          <font-awesome-icon :icon="['fas', 'graduation-cap']"/>
          Brevet des collèges
        </div>
      </div>
      <div class="high-school-thiers">
        <div class="location">
          <font-awesome-icon icon="fa-solid fa-location-pin"/>
          <span>Lycée Saint Joseph les Maristes</span>
        </div>
        <div class="duration">
          <font-awesome-icon icon="fa-solid fa-calendar"/>
          <span>2021 - 2022</span>
        </div>
      </div>
      <div class="high-school-thiers">
        <div class="location">
          <font-awesome-icon icon="fa-solid fa-location-pin"/>
          <span>Lycée Thiers</span>
        </div>
        <div class="duration">
          <font-awesome-icon icon="fa-solid fa-calendar"/>
          <span>2022 - 2024</span>
        </div>
        <div class="graduation">
          <font-awesome-icon :icon="['fas', 'graduation-cap']"/>
          Baccalauréat <i>(To come)</i>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.content {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-start;
  justify-content: center;

  padding: 1.5rem;
}

#experiences {
  border-left: solid .25rem var(--red);

  margin-left: 1rem;
  padding-left: 2rem;
  padding-top: 1rem;
  padding-bottom: 1rem;

  display: flex;
  flex-direction: column;
  gap: 2rem;

  & > * {
    position: relative;
    padding-top: 1.5rem;

    width: fit-content;

    &::before {
      content: '';

      display: block;

      width: 1.5rem;
      height: 1.5rem;

      border-radius: 9999rem;

      background-color: var(--red);

      position: absolute;
      top: 0;
      left: -2.125rem;
      transform: translateX(-50%);
    }

    &::after {
      content: '';

      display: block;

      width: calc(100%);
      height: .25rem;
      border-radius: 1rem;

      background-color: var(--red);

      position: absolute;
      left: 0;
      top: .75rem;
      transform: translateY(-50%);
    }

    & > * {
      display: flex;
      align-items: center;

      gap: .5rem;
    }
  }
}
</style>
<style lang="scss">
.svg-inline--fa {
  width: 24px;
}
</style>
