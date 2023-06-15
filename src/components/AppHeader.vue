<template>
    <header>
        <div class="wrapper">
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
        </div>
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
        height: 150px;
        background-color: red;

        div.wrapper {
            @include flex(row, space-around, center, no-wrap);
            @include w-75-centered;
            height: 100%;

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
    }
</style>