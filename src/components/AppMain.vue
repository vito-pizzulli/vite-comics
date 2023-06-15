<template>
    <main>
        <div class="wrapper">
            <h1>Content goes here</h1>
        </div>
    </main>
</template>
<script>
export default {
    name: 'AppMain'
}
</script>
<style lang="scss" scoped>
    @use '../styles/general' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    main {
        padding: 2rem 0;
        color: white;
        background-color: $bg_primary_color;

        div.wrapper {
            @include flex(row, start, center, no-wrap);
            @include w-75-centered;
            height: 100%;
        }
    }
</style>