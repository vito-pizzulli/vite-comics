<template>
    <div id="navbar-blue">
        <div class="wrapper">
            <ul>
                <li v-for="link in navbarLinks">
                    <img :src="link.image" :alt="link.text + ' Image'">
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
                    image: 'src/assets/img/buy-comics-digital-comics.png',
                    link: '#'
                },
                {
                    text: 'DC Merchandise',
                    image: 'src/assets/img/buy-comics-merchandise.png',
                    link: '#'
                },
                {
                    text: 'Subscription',
                    image: 'src/assets/img/buy-comics-subscriptions.png',
                    link: '#'
                },
                {
                    text: 'Comics Shop Locator',
                    image: 'src/assets/img/buy-comics-shop-locator.png',
                    link: '#'
                },
                {
                    text: 'DC Power Visa',
                    image: 'src/assets/img/buy-dc-power-visa.svg',
                    link: '#'
                }
            ]
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
        height: 200px;

        div.wrapper {
            @include flex(row, start, center, no-wrap);
            @include w-75-centered;
            height: 100%;
        }
    }
</style>