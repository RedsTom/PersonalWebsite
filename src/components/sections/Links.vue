<script setup lang="ts">
import Splitter from '../global/Splitter.vue';
</script>

<template>
    <Splitter>Some links</Splitter>

    <section id="links">
            <a href="https://github.com/RedsTom" class="link" target="_blank">
                <font-awesome-icon icon="fa-brands fa-github" />
                RedsTom
            </a>
            <a href="https://www.linkedin.com/in/tom-butin-807bab1b6" class="link" target="_blank">
                <font-awesome-icon icon="fa-brands fa-linkedin" />
                Tom BUTIN
            </a>
            <a href="https://youtube.com/c/RedsTom_" class="link" target="_blank">
                <font-awesome-icon icon="fa-brands fa-youtube" />
                RedsTom
            </a>
            <a href="https://discord.com/users/723471302123323434" class="link" target="_blank">
                <font-awesome-icon icon="fa-brands fa-discord" />
                redstom
            </a>
            <a href="https://twitch.tv/mr_redstom" class="link" target="_blank">
                <font-awesome-icon icon="fa-brands fa-twitch" />
                mr_redstom
            </a>
    </section>
</template>

<style lang="scss" scoped>
section {
    padding: 2rem;
}

section#links {
    font-size: 1.5rem;

    display: flex;
    justify-content: space-evenly;
    align-items: center;

    flex-wrap: wrap;

    gap: .5rem;

    a.link {
        margin: .5rem;
    }
}
</style>