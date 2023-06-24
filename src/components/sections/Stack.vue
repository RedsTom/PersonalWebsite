<script setup lang="ts">
import Splitter from '../global/Splitter.vue';
import StackElement from '../global/StackElement.vue';

interface StackElement {
  icon: string;
  name: string;
  year: number;
  link?: string;
}

const languages: StackElement[] = [
  {
    name: 'Java',
    icon: 'fa-brands fa-java',
    year: 2018,
  },
  {
    name: 'Python',
    icon: 'fa-brands fa-python',
    year: 2018,
  },
  {
    name: 'PHP',
    icon: 'fa-brands fa-php',
    year: 2019,
  },
  {
    name: 'HTML / CSS',
    icon: 'fa-brands fa-html5',
    year: 2019,
  },
  {
    name: 'Javascript',
    icon: 'fa-brands fa-square-js',
    year: 2020,
  },
  {
    name: 'Typescript',
    icon: 'fa-brands fa-square-js',
    year: 2020,
  },
]

const technologies: StackElement[] = [
  {
    name: 'Discord Bots',
    icon: 'fa-solid fa-robot',
    year: 2019,
    link: 'https://discord.dev/'
  },
  {
    name: 'VueJS',
    icon: 'fa-brands fa-vuejs',
    year: 2019,
    link: 'https://vuejs.org/'
  },
  {
    name: 'Git',
    icon: 'fa-brands fa-git',
    year: 2020,
    link: 'https://github.com/'
  },
  {
    name: 'Node.js',
    icon: 'fa-brands fa-node-js',
    year: 2020,
    link: 'https://nodejs.org/'
  },
  {
    name: 'Spring',
    icon: 'fa-solid fa-leaf',
    year: 2021,
    link: 'https://spring.io/'
  },
  {
    name: 'PostgreSQL',
    icon: 'fa-solid fa-database',
    year: 2021,
    link: 'https://postgresql.org/'
  },
  {
    name: 'React',
    icon: 'fa-brands fa-react',
    year: 2021,
    link: 'https://reactjs.org/'
  },
]

const softwares: StackElement[] = [
  {
    name: 'Eclipse',
    icon: 'fa-solid fa-code',
    year: 2018,
    link: 'https://eclipse.org/'
  },
  {
    name: 'VS Code',
    icon: 'fa-solid fa-code',
    year: 2019,
    link: 'https://code.visualstudio.com/'
  },
  {
    name: 'IntelliJ IDEA',
    icon: 'fa-solid fa-code',
    year: 2019,
    link: 'https://jetbrains.com/idea'
  },
  {
    name: 'PhpStorm',
    icon: 'fa-solid fa-code',
    year: 2020,
    link: 'https://jetbrains.com/phpstorm'
  },
  {
    name: 'Figma',
    icon: 'fa-brands fa-figma',
    year: 2020,
    link: 'https://figma.com'
  }
]
</script>

<template>
  <Splitter>My stack</Splitter>

  <section id="stack">
    <div>
      <h3><b>&lt;</b>Programming languages<b> /&gt;</b></h3>

      <ul>
        <StackElement v-for="(language, index) in languages" :icon="language.icon" :year="language.year"
                      :link="language.link" :key="language.name" :first="index === 0"
                      :last="index === languages.length - 1">
          {{ language.name }}
        </StackElement>
      </ul>
    </div>
    <div class="splitter"></div>
    <div>
      <h3><b>&lt;</b>Technologies<b> /&gt;</b></h3>

      <ul>
        <StackElement v-for="(techno, index) in technologies" :icon="techno.icon" :year="techno.year" :link="techno.link"
                      :key="techno.name" :first="index === 0" :last="index === technologies.length - 1">
          {{ techno.name }}
        </StackElement>
      </ul>
    </div>
    <div class="splitter"></div>
    <div>
      <h3><b>&lt;</b>Softwares<b> /&gt;</b></h3>

      <ul>
        <StackElement v-for="(editor, index) in softwares" :icon="editor.icon" :year="editor.year" :link="editor.link"
                      :key="editor.name" :first="index === 0" :last="index === softwares.length - 1">
          {{ editor.name }}
        </StackElement>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
#stack {
  display: grid;
  grid-template-columns: 1fr 0 1fr 0 1fr;
  grid-gap: 2rem;

  padding: 1rem;

  @media screen and (max-width: 1150px) {
    display: flex;
    flex-direction: column;
    grid-gap: 1rem;

    padding-bottom: 2rem;

    grid-template-columns: none;
  }

  & > div {
    display: flex;
    flex-direction: column;
    gap: 1rem;

    padding-bottom: 1rem;

    @media screen and (max-width: 1150px) {
      padding-bottom: 0;
    }
  }

  b {
    color: var(--primary-text);
  }

  h3 {
    text-align: center;

    @media screen and (max-width: 1150px) {
      text-align: start;
    }
  }

  .splitter {
    width: .25rem;
    height: 100%;

    border-radius: 9999px;

    background-color: var(--text);

    @media screen and (max-width: 1150px) {
      display: none;
    }
  }

  ul {
    list-style: none;

    font-size: 1.25rem;

    display: flex;
    flex-direction: column;
    justify-content: center;

    height: fit-content;

    @media screen and (max-width: 1150px) {
      padding-left: 2rem;
    }
  }
}
</style>