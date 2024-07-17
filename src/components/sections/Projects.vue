<script setup lang="ts">
import Project from '../global/Project.vue';

import findTheCoin from '../../assets/find-the-coin.png';
import privateRooms from '../../assets/private-rooms.svg';
import youtube from '../../assets/youtube.jpg'
import frlang from '../../assets/frlang.svg';
import sfcord from '../../assets/sfcord.png';
import brainfuck from '../../assets/brainfuck.png';
import developpons from '../../assets/developpons.png';

import Splitter from '../global/Splitter.vue';
</script>

<template>
    <Splitter>My projects</Splitter>
    <section id="projects">
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
        <Project :bg="sfcord" href="https://github.com/SFCord/">
            SFCord
        </Project>
        <Project :bg="brainfuck" href="https://github.com/RedsTom/BrainfuckInterpreter">
            My Brainfuck Interpreter
        </Project>
        <Project :bg="developpons" href="https://discord.gg/RuRT6aVhHu">
            My Discord Server
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
