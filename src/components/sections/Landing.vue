<script setup lang="ts">
import moment from 'moment';
import Switch from '../global/Switch.vue';

const age = moment().diff('2006-07-06', 'years');
</script>

<template>
  <section id="landing">
    <div class="left">
      <h1>
        Hi, I'm <b>RedsTom</b>:<br class="breakline"/>
        a <b>
          <Switch :elements="['java', 'web', 'spring', 'junior', 'vue.js']" :delay="10_000" />
        </b> developer<b>.</b>
      </h1>

      <div class="quote-container">
        <p class="quote">
          <img draggable="false" alt="quote" src="../../assets/quote.svg" height="36" />
          Grown-ups never understand anything by themselves, and it is tiresome for children to be always and forever explaining things to them.
        </p>
        <span class="author">Antoine de Saint Exupéry, <u>Le petit prince</u></span>
      </div>
    </div>
    <div class="splitter"></div>
    <div class="right">
      <ul>
        <li>🎂 {{age}} years old<b>.</b></li>
        <li>📍 Marseille, France<b>.</b></li>
        <li>🏫 Lycée Thiers<b>.</b></li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
#landing {
  font-size: 1.5rem;

  padding: 3rem;

  display: grid;
  grid-template-columns: 3fr 0 1fr;
  grid-gap: 4rem;

  @media screen and (max-width: 1400px) {
    grid-template-columns: 1fr;
    grid-template-rows: 2fr 0 1fr;

    grid-gap: 2rem;
    padding: 2rem 2rem 0;
  }

  br {
    display: none;

    @media screen and (max-width: 800px) {
      display: block;
    }
  }

  b {
    color: var(--primary-text);
    font-weight: bold;
  }

  .left {
    display: flex;
    justify-content: center;

    flex-direction: column;
    grid-gap: 1rem;

    padding-bottom: 1rem;

    .quote-container {
      display: flex;
      flex-direction: column;

      .author {
        margin-top: .5rem;

        align-self: flex-end;
        font-size: 1.25rem;

        font-style: italic;
      }
    }

    .quote {
      display: grid;
      grid-template-columns: 0fr 9fr;
      grid-gap: .5rem;

      text-align: justify;

      img {
        display: flex;
      }
    }
  }

  .splitter {
    width: .25rem;
    height: 100%;

    border-radius: 9999px;

    background-color: var(--text);

    @media screen and (max-width: 1400px) {
      height: .25rem;
      width: 100%;
    }
  }

  .right {
    display: flex;
    align-items: center;

    @media screen and (max-width: 800px) {
      justify-content: center;
    }

    ul {
      list-style: none;

      @media screen and (max-width: 1400px) {
        width: 100%;

        display: flex;
        justify-content: space-evenly;
      }

      @media screen and (max-width: 800px) {
        width: fit-content;
        flex-direction: column;
      }

      li {
        align-items: center;
        width: fit-content;
      }
    }
  }
}
</style>