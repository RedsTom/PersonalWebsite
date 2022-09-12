<script lang="ts" setup>
const props = defineProps<{
    bg?: string,
    href?: string,
}>();

const wd = window;
</script>

<template>
    <div class="project">
        <div class="link" :style="{ backgroundImage: `url(${props.bg})` }" @click="wd.open(props.href)">
        </div>
        <a class="description" :href="props.href">
            <slot />
        </a>
    </div>
</template>

<style lang="scss" scoped>
.project {
    display: flex;
    flex-direction: column;

    justify-content: center;
    align-items: center;
}

.link {
    cursor: pointer;

    width: 16rem;
    height: 10em;

    background: var(--text);

    transition: .2s;

    background-color: var(--white);
    background-position: center;
    background-size: cover;

    display: flex;
    justify-content: center;
    align-items: center;

    border-radius: .5rem;

    &:hover {
        transform: translate(-1rem, -1rem);
        box-shadow: 1rem 1rem 0 var(--primary-text);
    }
}

.description {
    width: 100%;
    text-decoration: none;

    text-align: center;

    padding: .75rem 0;
    font-size: 1.25rem;
}
</style>