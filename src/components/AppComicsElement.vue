<template>
    <div class="comics-element">
        <img :src="comicsElement.thumb" :alt="comicsElement.series"><br>
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
        width: calc(100% / 6 - 1rem);
        margin: 2rem 0;
        cursor: pointer;
        text-align: center;
        transition: all .2s ease;
        height: 300px;

        &:hover {
            transform: scale(1.05);
        }

        img {
            max-width: 190px;
            height: 300px;
        }

        span {
            text-transform: uppercase;
        }
    }
</style>