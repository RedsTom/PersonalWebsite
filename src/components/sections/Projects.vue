<script setup lang="ts">
import Project from '../global/Project.vue';

import findTheCoin from '../../assets/find-the-coin.png';
import privateRooms from '../../assets/private-rooms.svg';
import youtube from '../../assets/youtube.jpg'
import frlang from '../../assets/frlang.svg';
import tidalcord from '../../assets/tidalcord.png';

import Splitter from '../global/Splitter.vue';
</script>

<template>
    <Splitter>My projects</Splitter>
    <section id="projects">
        <Project :bg="tidalcord" href="https://github.com/RedsTom/Tidalcord/">
            TidalCord
        </Project>
        <Project :bg="findTheCoin" href="https://findthecoin.redstom.fr/">
            Find the Coins
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
  display: grid;
  grid-template-columns: repeat(auto-fit, 256px);
  justify-content: space-evenly;
  align-items: center;
  align-content: center;

  gap: 2rem;

  width: 100%;
}
</style>
