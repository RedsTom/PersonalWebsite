<script lang="ts" setup>
import {ref} from 'vue';
import Splitter from '../global/Splitter.vue';

const subject = ref('');
const body = ref('');

const send = () => {
  if (subject.value && body.value) {
    // @ts-ignore
    window.location = `mailto:tom.frefre.13@gmail.com?subject=${subject.value}&body=${body.value.replace('\n', '%0D%0A')}`;
  }
}
</script>

<template>
  <Splitter>Contact me</Splitter>

  <section id="contact">
    <form @submit.prevent="send">
      <input title="Object" placeholder="Subject" v-model="subject"/>
      <textarea title="Body" placeholder="Body" v-model="body"/>
      <button type="submit">Send</button>
    </form>
  </section>
</template>

<style lang="scss" scoped>
#contact {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 100%;
  height: calc(100% - 3rem);

  padding: 2rem;

  form {
    display: flex;
    flex-direction: column;
    gap: 1rem;

    width: 100%;
    height: 100%;

    & > * {
      width: 100%;
    }

    input,
    textarea,
    button {
      outline: none;
      background-color: transparent;

      border-radius: .5rem;

      font-size: 1rem;

      border: var(--red) solid 4px;
      transition: .2s;

      &:focus {
        border-color: var(--green);
      }
    }

    input,
    textarea {
      padding: 1rem;
    }

    input,
    button {
      height: 5rem;
    }

    button {
      color: var(--red);

      &:hover {
        border-color: var(--red);
        color: var(--text);
        background-color: var(--red);
      }

      &:focus:not(:hover) {
        color: var(--green);
      }

      &:active {
        border-color: var(--green);
        color: var(--text);
        background-color: var(--green);
      }
    }

    textarea {
      min-height: 10rem;
      height: 100%;
      resize: none;
    }
  }
}
</style>
