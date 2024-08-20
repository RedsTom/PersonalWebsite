<script setup lang="ts">

import Splitter from "../global/Splitter.vue";
</script>

<template>
  <Splitter>My Scholar Career</Splitter>

  <div class="content">
    <div id="experiences">
      <div class="license-luminy">
        <div class="location">
          <font-awesome-icon icon="fa-solid fa-location-pin" />
          <span>Université d'<u>Aix-Marseille</u> - <u>Luminy</u></span>
        </div>
        <div class="duration">
          <font-awesome-icon icon="fa-solid fa-calendar" />
          2024 - Présent
        </div>
        <div class="graduation">
          <font-awesome-icon :icon="['fas', 'graduation-cap']"/>
          <span>
            Double License <u>Maths-Info</u>
          </span>
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
          <span>
            Baccalauréat mention <u>Bien</u> (15.8/20)<br/>
            <ul>
              <li>Maths : <u>20/20</u></li>
              <li>PH-CH : <u>20/20</u></li>
            </ul>
          </span>
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
          <span>
            Brevet des collèges mention <u>Très Bien</u> (19.9/20)
          </span>
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

u {
  padding: 0;
  margin: 0;

  text-decoration: none;
  color: var(--red);

  display: inline-flex;
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

      padding: .5rem 0;

      gap: .5rem;

      span {
        display: block;
      }
    }

  }
}
ul {
  margin-left: 1rem;
}
</style>
<style lang="scss">
.svg-inline--fa {
  width: 24px;
}
</style>
