<script setup lang="ts">
const props = defineProps<{ text: string }>();
</script>

<template>
  <span v-for="l in props.text" :key="l">
    {{ l }}
  </span>
</template>