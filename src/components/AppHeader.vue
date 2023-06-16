<template>
    <header>
        <div class="wrapper">
            <div id="header-logo">
            <img src="../assets/img/dc-logo.png" alt="DC Comics Logo">
        </div>
        <nav id="header-navbar">
            <ul>
                <li v-for="link in navbarLinks">
                    <a :href="link.link">{{ link.text }}</a>
                    <div class="light-bar"></div>
                </li>
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
                        text: 'Characters',
                        link: '#'
                    },
                    {
                        text: 'Comics',
                        link: '#'
                    },
                    {
                        text: 'Movies',
                        link: '#'
                    },
                    {
                        text: 'TV',
                        link: '#'
                    },
                    {
                        text: 'Games',
                        link: '#'
                    },
                    {
                        text: 'Collectibles',
                        link: '#'
                    },
                    {
                        text: 'Videos',
                        link: '#'
                    },
                    {
                        text: 'Fans',
                        link: '#'
                    },
                    {
                        text: 'News',
                        link: '#'
                    },
                    {
                        text: 'Shop',
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
        padding: 1rem 0;
        
        div.wrapper {
            @include flex(row, space-between, center, no-wrap);
            height: 100%;

            nav#header-navbar {

                ul {
                    @include flex(row, space-between, center, no-wrap);

                    li {
                        margin: 1rem;
                        text-transform: uppercase;
                        font-weight: 600;
                        position: relative;

                        &:hover div.light-bar {
                            opacity: 1;
                        }

                        a {
                            transition: all .3s;

                            &:hover {
                                color: $primary_color;
                            }
                        }

                        div.light-bar {
                            position: absolute;
                            width: 100%;
                            height: 7px;
                            background-color: $primary_color;
                            top: 335%;
                            opacity: 0;
                            transition: all .3s;
                        }
                    }
                }
            }
        }
    }
</style>