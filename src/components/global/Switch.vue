<script setup lang="ts">
import { ElementTypes } from '@vue/compiler-core';
import { computed, ref } from 'vue';

const props = withDefaults(defineProps<{ elements: string[], delay?: number, typingSpeed?: number }>(), {
    delay: 1000,
    typingSpeed: 100,
});

const index = ref(0);
const text = ref('');

const type = (word: string): void => {
    const length = text.value.length;

    for (let i = 0; i < length; i++) {
        setTimeout(() => {
            text.value = text.value.substring(0, text.value.length - 1);
        }, (i) * props.typingSpeed);
    }

    for (let i = 0; i < word.length; i++) {
        setTimeout(() => {
            text.value += word[i];
        }, (i + length + 2) * props.typingSpeed);
    }
}

type(props.elements[index.value]);
setInterval(() => {
    let random = Math.floor(Math.random() * props.elements.length);
    if (random == index.value) {
        random = random == props.elements.length - 1 ? 0 : random + 1;
    }
    index.value = random;

    type(props.elements[index.value]);
}, props.delay);
</script>

<template>
    {{ text }}<span class="carret">|</span>
</template>

<style lang="scss" scoped>
.carret {
    animation: carret infinite 1s linear;
    font-weight: 200;

    user-select: none;
}

@keyframes carret {
    5% {
        opacity: 0;
    }

    45% {
        opacity: 0;
    }

    55% {
        opacity: 1;
    }

    95% {
        opacity: 1;
    }
}
</style>