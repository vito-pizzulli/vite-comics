<template>
    <footer>
        <div class="upper-footer">
            <div class="wrapper">
                <div>
                    <ul>
                        <li><h3>PROVA</h3></li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                    </ul>
                    <ul>
                        <li><h3>PROVA</h3></li>
                        <li>Prova</li>
                        <li>Prova</li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li><h3>PROVA</h3></li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li><h3>PROVA</h3></li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                        <li>Prova</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="bottom-footer">
            <div class="wrapper">
                <div class="sign-up">
                    <button>Sign-up now!</button>
                </div>
                <div class="follow-us">
                    <ul>
                        <li>Follow us</li>
                        <li><img src="../assets/img/footer-facebook.png" alt="Facebook Logo"></li>
                        <li><img src="../assets/img/footer-twitter.png" alt="Twitter Logo"></li>
                        <li><img src="../assets/img/footer-youtube.png" alt="YouTube Logo"></li>
                        <li><img src="../assets/img/footer-pinterest.png" alt="Pinterest Logo"></li>
                        <li><img src="../assets/img/footer-periscope.png" alt="Periscope Logo"></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>
<script>
export default {
    name: 'AppFooter'
}
</script>
<style lang="scss" scoped>
    @use '../styles/general' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    footer {

        div.upper-footer {
            color: $txt_secondary_color;
            background-image: url(../assets/img/footer-bg.jpg);
            background-repeat: no-repeat;
            background-size: cover;
            height: 500px;

            div.wrapper {
                @include flex(row, start, start, no-wrap);
                @include w-75-centered;
                height: 100%;

                ul {
                    padding: 0;

                    li {
                        margin: 1rem;
                    }
                }
            }
        }

        div.bottom-footer {
            color: white;
            background-color: $bg_secondary_color;
            height: 150px;
            
            div.wrapper {
                @include flex(row, space-between, center, no-wrap);
                @include w-75-centered;
                height: 100%;

                div.follow-us {

                    ul {
                        @include flex(row, center, center, no-wrap);

                        li {
                            margin: .5rem;
                        }
                    }
                }
            }
        }
    }

</style>