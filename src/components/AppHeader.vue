<template>
    <header>
        <div class="wrapper">
            <div id="header-logo">
            <img src="../assets/img/dc-logo.png" alt="DC Comics Logo">
        </div>
        <nav id="header-navbar">
            <ul>
                <li v-for="link in navbarLinks"><a :href="link.link">{{ link.text }}</a></li>
            </ul>
        </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',

    data() {
            return {
                navbarLinks: [
                    {
                        text: 'characters',
                        link: '#'
                    },
                    {
                        text: 'comics',
                        link: '#'
                    },
                    {
                        text: 'movies',
                        link: '#'
                    },
                    {
                        text: 'tv',
                        link: '#'
                    },
                    {
                        text: 'games',
                        link: '#'
                    },
                    {
                        text: 'collectibles',
                        link: '#'
                    },
                    {
                        text: 'videos',
                        link: '#'
                    },
                    {
                        text: 'fans',
                        link: '#'
                    },
                    {
                        text: 'news',
                        link: '#'
                    },
                    {
                        text: 'shop',
                        link: '#'
                    },
                ]
            }
        }
}
</script>

<style lang="scss" scoped>
    @use '../styles/general' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    header {
        height: 150px;
        
        div.wrapper {
            @include flex(row, space-around, center, no-wrap);
            @include w-75-centered;
            height: 100%;

            nav#header-navbar {

                ul {
                    @include flex(row, space-between, center, no-wrap);

                    li {
                        margin: 1rem;
                    }
                }
            }
        }
    }
</style>