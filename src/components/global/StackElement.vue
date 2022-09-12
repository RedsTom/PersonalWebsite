<script setup lang="ts">
interface Props {
    icon: string;
    year: number;
    link?: string;
}

const props = defineProps<Props>();
</script>

<template>
    <li class="stack-element">
        <font-awesome-icon :icon="props.icon" />
        <p>
            <slot />
            <a v-if="props.link" :href="props.link" target="_blank">
                <font-awesome-icon icon="fa-solid fa-link" />
            </a>
        </p>
        <div class="splitter"></div>
        <span><b>{{ props.year }}</b></span>
    </li>
</template>

<style lang="scss">
li.stack-element {
    display: grid;
    grid-template-columns: 1rem 10fr 0 3fr;
    gap: 1rem;

    align-items: center;

    @media screen and (max-width: 1660px) {
        grid-template-columns: 1rem 10fr 0 5fr;
    }

    * {
        overflow: hidden;
        text-overflow: ellipsis;
    }

    svg {
        display: flex;
        align-items: center;

        path {
            fill: var(--red)
        }
    }

    span {
        text-align: end;
    }

    p {
        display: flex;
        gap: .5rem;
        align-items: center;

        a {
            transition: .2s;

            &:hover {
                transform: scale(1.25);
            }
        }

        svg {
            font-size: 1rem;

            path {
                fill: var(--green);
            }
        }
    }

    .splitter {
        width: .25rem;
        height: 100%;

        border-radius: 9999px;

        background-color: var(--text);
    }

    b {
        color: var(--blue);
    }
}
</style>