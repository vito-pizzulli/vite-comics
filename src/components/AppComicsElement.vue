<template>
    <div class="comics-element">
        <img :src="comicsElement.thumb" :alt="comicsElement.series">
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
        margin: 1rem 0;

        img {
            width: 180px;
            height: 250px;
        }
    }
</style>