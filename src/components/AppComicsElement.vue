<template>
    <div class="comics-element">
        <img :src="comicsElement.thumb" :alt="comicsElement.series">
        <span>{{ comicsElement.series }}</span>
    </div>
</template>

<script>
export default {
    name: 'AppComicsElement',

    props: {
        comicsElement : Object
    }
}
</script>

<style lang="scss" scoped>
    @use '../styles/general' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    div.comics-element {
        width: calc(100% / 6);
        margin: 2rem .5rem;
        width: 170px;
        height: 250px;
        cursor: pointer;
        text-align: center;
        transition: all .2s ease;

        &:hover {
            transform: scale(1.1);
        }

        img {
            width: 170px;
            height: 250px;
        }

        span {
            text-transform: uppercase;
        }
    }
</style>