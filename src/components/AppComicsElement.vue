<template>
    <div class="comics-element">
        <h1>{{ comicsELement }}</h1>
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
</style>