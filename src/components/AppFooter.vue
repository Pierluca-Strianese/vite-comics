<script>

import NavBarFooter from './NavBarFooter.vue';

export default {
    data() {
        return {
            comics: [
                "Characters",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News"
            ],
            shops: [
                "Shop DC",
                "Shop DC Collectibles"
            ],
            DC: [
                "Terme of Use",
                "Privacy Policy (New)",
                "Ad Choices",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshop",
                "CPCS Certificates",
                "Ratings",
                "Shop Help",
                "Contact us"
            ],
            sites: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ],
            socials: [
                "footer-facebook.png",
                "footer-twitter.png",
                "footer-youtube.png",
                "footer-pinterest.png",
                "footer-periscope.png"
            ]
        }
    },

    components: {
        NavBarFooter
    },

    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },
    },
};

</script>

<template>
    <NavBarFooter />
    <footer>

        <section class="links">
            <div class="container">
                <div class="cols">

                    <!-- colonna sx -->
                    <div class="col">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="comic in comics">
                                <a href="#">{{ comic }}</a>
                            </li>
                        </ul>

                        <h3 class="mt-top">SHOP</h3>
                        <ul>
                            <li v-for="shop in shops">
                                <a href="#">{{ shop }}</a>
                            </li>
                        </ul>
                    </div>

                    <!-- colonna centrale -->
                    <div class="col center">
                        <h3>DC</h3>
                        <ul>
                            <li v-for="link in DC">
                                <a href="#">{{ link }}</a>
                            </li>
                        </ul>
                    </div>

                    <!-- colonna dx -->
                    <div class="col">
                        <h3>SITES</h3>
                        <ul>
                            <li v-for="site in sites">
                                <a href="#"> {{ site }}</a>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="bg-logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>

            </div>

        </section>

        <section class="sub-footer">

            <div class="container">

                <a class="sign-up">SIGN-UP NOW!</a>

                <div class="social">
                    <span>FOLLOW US</span>
                    <ul>
                        <li v-for="social in socials">
                            <img :src="getImagePath(social)" alt="">
                        </li>
                    </ul>
                </div>
            </div>

        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;

footer {

    ul {
        list-style-type: none;
        padding-left: 0;
        margin-left: 0;
    }

    h3 {
        font-size: 1rem;
    }

    .links {
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        color: $text-white;

        .container {
            display: flex;
            position: relative;
            overflow: hidden;

            .cols {
                display: flex;

                .col {
                    padding: 30px 0;

                    .mt-top {
                        margin-top: 20px;
                    }

                    a {
                        color: #5f5f5f;
                        font-size: .8rem;
                        text-decoration: none;
                    }

                    &.center {
                        padding-inline: 30px;
                    }
                }
            }

            .bg-logo {
                width: 500px;
                height: 350px;
            }

            .bg-logo img {
                position: absolute;
                right: 0;
                top: -80px;
            }
        }

    }

    .sub-footer {
        height: 90px;
        background-color: #303030;

        .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 100%;

            .sign-up {
                height: fit-content;
                display: flex;
                align-items: center;
                color: $text-white;
                padding: 10px;
                border: 2px solid $primary;
            }

            .social {
                display: flex;
                align-items: center;

                ul {
                    display: flex;
                    align-items: center;
                    margin: 0;

                    li {
                        padding: 0 10px;
                    }
                }

                span {
                    color: $primary;
                }
            }
        }
    }
}
</style>