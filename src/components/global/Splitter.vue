<template>
    <div class="splitter">
        <h2 class="content">
            <slot />
        </h2>
    </div>
</template>

<style lang="scss" scoped>
.splitter {
    display: flex;
    align-items: center;
    grid-gap: 1rem;

    width: 100%;

    text-align: center;

    &::before,
    &::after {
        content: '';
        height: .25rem;
        width: 100%;

        border-radius: 9999px;

        background-color: var(--text);
    }

    .content {
        min-width: fit-content;
    }
}
</style>