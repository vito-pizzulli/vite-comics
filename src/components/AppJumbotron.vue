<template>
    <div id="jumbotron">
        <img src="../assets/img/jumbotron.jpg" alt="DC Comics Jumbotron">
    </div>
</template>

<script>
export default {
    name: 'AppJumbotron'
}
</script>

<style lang="scss">
    @use '../styles/general' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    div#jumbotron {
        height: 600px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }
</style>