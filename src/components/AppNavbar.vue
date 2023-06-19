<template>
    <div id="navbar-blue">
        <div class="wrapper">
            <ul>
                <li v-for="link in navbarLinks">
                    <img :src="getImagePath(link.image)" :alt="link.text + ' Image'">
                    <a :href="link.link">{{ link.text }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppNavbar',

    data() {
        return {
            navbarLinks: [
                {
                    text: 'Digital comics',
                    image: 'img/buy-comics-digital-comics.png',
                    link: '#'
                },
                {
                    text: 'DC Merchandise',
                    image: 'img/buy-comics-merchandise.png',
                    link: '#'
                },
                {
                    text: 'Subscription',
                    image: 'img/buy-comics-subscriptions.png',
                    link: '#'
                },
                {
                    text: 'Comics Shop Locator',
                    image: 'img/buy-comics-shop-locator.png',
                    link: '#'
                },
                {
                    text: 'DC Power Visa',
                    image: 'img/buy-dc-power-visa.svg',
                    link: '#'
                }
            ]
        }
    },
    methods: {
        getImagePath: function(img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}
</script>

<style lang="scss" scoped>
    @use '../styles/general' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    div#navbar-blue {
        background-color: $primary_color;
        padding: 3.5rem 0;

        div.wrapper {
            @include flex(row, center, center, no-wrap);
            height: 100%;

            ul {
                @include flex(row, space-around, center, no-wrap);
                width: 100%;

                li {
                    @include flex(row, center, center, no-wrap);

                    img {
                        height: 70px;
                        max-width: 70px;
                        margin-right: 1rem;
                    }

                    a {
                        text-transform: uppercase;
                        color: white;
                    }
                }
            }
        }
    }
</style>