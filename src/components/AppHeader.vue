<template>
    <header>
        <div id="header-logo">
            <img src="../assets/img/dc-logo.png" alt="DC Comics Logo">
        </div>
        <nav id="header-navbar">
            <ul>
                <li>Prova</li>
                <li>Prova</li>
                <li>Prova</li>
                <li>Prova</li>
                <li>Prova</li>
                <li>Prova</li>
                <li>Prova</li>
                <li>Prova</li>
            </ul>
        </nav>
    </header>
</template>
<script>
export default {
    name: 'AppHeader'
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    header {
        @include flex(row, space-around, center, no-wrap);
        @include w-75-centered;
        height: 150px;
        background-color: red;
        
        nav#header-navbar {

            ul {
            @include flex(row, space-between, center, no-wrap);
            list-style: none;

                li {
                    margin: 1rem;
                }
            }
        }
    }
</style>