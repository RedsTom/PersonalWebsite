<script setup lang="ts">
import Project from '../global/Project.vue';

import gravenDev from '../../assets/graven-dev.svg';
import privateRooms from '../../assets/private-rooms.svg';
import youtube from '../../assets/youtube.jpg'
import frlang from '../../assets/frlang.svg';
import Separator from '../global/Separator.vue';
import Splitter from '../global/Splitter.vue';
</script>

<template>
    <Splitter>My projects</Splitter>
    <section id="projects">
        <Project :bg="gravenDev" href="https://discord.gg/graven">
            Graven - Développement
        </Project>
        <Project :bg="privateRooms" href="https://github.com/GravenDev/PrivateRooms">
            Private Rooms
        </Project>
        <Project :bg="youtube" href="https://youtube.com/c/RedsTom_">
            YouTube Channel
        </Project>
        <Project :bg="frlang" href="https://github.com/FrLang/">
            FrLang
        </Project>
    </section>
</template>

<style lang="scss" scoped>
section {
    padding: 2rem;
}

section#projects {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    align-content: center;

    flex-wrap: wrap;
    gap: 2rem;
}
</style>