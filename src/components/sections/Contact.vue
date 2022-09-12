<script lang="ts" setup>
import Splitter from '../global/Splitter.vue';

</script>

<template>
    <Splitter>Contact me</Splitter>

    <section id="contact">
        <p>
            If you need more informations, contact me at <a class="link"
                href="mailto:contact@redstom.me">contact@redstom.me</a> or <a href="mailto:tom.frefre.13@gmail.com"
                class="link">tom.frefre.13@gmail.com</a>
        </p>
    </section>
</template>

<style lang="scss" scoped>
#contact {
    display: flex;
    align-items: center;
}

p {
    padding: 1rem;

    text-align: center;
    font-size: 1.25rem;
}

a {
    color: var(--green);
    margin-right: .75rem;
}
</style>