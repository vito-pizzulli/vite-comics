<template>
    <footer>
        <div id="upper-footer">
            <div class="wrapper">
                <div id="upper-footer-elements">
                    <div>
                        <ul>
                            <li><h3>DC Comics</h3></li>
                            <li v-for="link in dcComicsLinks"><a :href="link.link">{{ link.text }}</a></li>
                        </ul>
                        <ul>
                            <li><h3>Shop</h3></li>
                            <li v-for="link in shopLinks"><a :href="link.link">{{ link.text }}</a></li>
                        </ul>
                    </div>
                    <div>
                        <ul>
                            <li><h3>DC</h3></li>
                            <li v-for="link in dcLinks"><a :href="link.link">{{ link.text }}</a></li>
                        </ul>
                    </div>
                    <div>
                        <ul>
                            <li><h3>Sites</h3></li>
                            <li v-for="link in sitesLinks"><a :href="link.link">{{ link.text }}</a></li>
                        </ul>
                    </div>
                </div>
                <div id="upper-footer-background-logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="DC Comics Background Logo">
                </div>
            </div>
        </div>
        <div id="bottom-footer">
            <div class="wrapper">
                <div class="sign-up">
                    <button>Sign-up now!</button>
                </div>
                <div class="follow-us">
                    <ul>
                        <li>Follow us</li>
                        <li v-for="social in socials"><a :href="social.link"><img :src="getImagePath(social.image)" :alt="social.text"></a></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',

    data() {
        return {
            dcComicsLinks: [
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
                    text: 'Videos',
                    link: '#'
                },
                {
                    text: 'News',
                    link: '#'
                }
            ],
            shopLinks: [
                {
                    text: 'Shop DC',
                    link: '#'
                },
                {
                    text: 'Shop DC Collectibles',
                    link: '#'
                }
            ],
            dcLinks: [
                {
                    text: 'Terms Of Use',
                    link: '#'
                },
                {
                    text: 'Privacy policy (New)',
                    link: '#'
                },
                {
                    text: 'Ad Choices',
                    link: '#'
                },
                {
                    text: 'Advertising',
                    link: '#'
                },
                {
                    text: 'Jobs',
                    link: '#'
                },
                {
                    text: 'Subscriptions',
                    link: '#'
                },
                {
                    text: 'Talent Workshops',
                    link: '#'
                },
                {
                    text: 'CPSC Certificates',
                    link: '#'
                },
                {
                    text: 'Ratings',
                    link: '#'
                },
                {
                    text: 'Shop Help',
                    link: '#'
                },
                {
                    text: 'Contact Us',
                    link: '#'
                }
            ],
            sitesLinks: [
                {
                    text: 'DC',
                    link: '#'
                },
                {
                    text: 'MAD Magazine',
                    link: '#'
                },
                {
                    text: 'DC Kids',
                    link: '#'
                },
                {
                    text: 'DC Universe',
                    link: '#'
                },
                {
                    text: 'DC Power Visa',
                    link: '#'
                }
            ],
            socials: [
                {
                    text: 'Facebook',
                    image: 'img/footer-facebook.png',
                    link: '#'
                },
                {
                    text: 'Twitter',
                    image: 'img/footer-twitter.png',
                    link: '#'
                },
                {
                    text: 'YouTube',
                    image: 'img/footer-youtube.png',
                    link: '#'
                },
                {
                    text: 'Pinterest',
                    image: 'img/footer-pinterest.png',
                    link: '#'
                },
                {
                    text: 'Periscope',
                    image: 'img/footer-periscope.png',
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

    footer {

        div#upper-footer {
            background-image: url(../assets/img/footer-bg.jpg);
            background-repeat: no-repeat;
            background-size: cover;
            padding: 3rem 0;
            overflow: hidden;

            div.wrapper {
                @include w-75-centered;
                @include flex(row, space-between, start, no-wrap);
                height: 100%;

                div#upper-footer-elements {
                    @include flex(row, start, start, no-wrap);

                    ul {
                    padding: 0;
                    margin-right: 2rem;

                        li {
                            margin: .3rem;

                            a {
                                color: $secondary_color;
                                transition: all .3s;

                                &:hover {
                                color: white;
                                }
                            }

                            h3 {
                                text-transform: uppercase;
                                color: white;
                                margin-bottom: 1rem;
                            }
                        }
                    }
                }

                div#upper-footer-background-logo img {
                    width: 400px;
                    transform: scale(2);
                    transform-origin: right;
                }
            }
        }

        div#bottom-footer {
            color: white;
            background-color: $bg_secondary_color;
            padding: 1rem 0;
            
            div.wrapper {
                @include flex(row, space-between, center, no-wrap);
                @include w-75-centered;
                height: 100%;

                div.sign-up {

                    button {
                        text-transform: uppercase;
                        background-color: transparent;
                        color: white;
                        padding: 1rem;
                        border: 2px solid $primary_color;
                        font-weight: 600;
                        font-size: 1rem;
                    }
                }

                div.follow-us {

                    ul {
                        @include flex(row, center, center, no-wrap);

                        li {
                            margin: .5rem;
                            text-transform: uppercase;
                            font-weight: 600;
                            color: $primary_color;
                            font-size: 1.5rem;

                            img {
                                vertical-align: bottom;
                            }
                        }
                    }
                }
            }
        }
    }

</style>