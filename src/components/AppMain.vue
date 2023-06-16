<template>
    <main>
        <AppComicsList />
        <AppNavbar />
    </main>
</template>

<script>
import AppComicsList from './AppComicsList.vue';
import AppNavbar from './AppNavbar.vue';
export default {
    name: 'AppMain',

    components: {
        AppComicsList,
        AppNavbar,
    }
}
</script>

<style lang="scss" scoped>
    @use '../styles/general' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    main {
        color: white;
        background-color: $bg_primary_color;
    }
</style>