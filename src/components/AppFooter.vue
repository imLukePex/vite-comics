<script>
export default {
    name: "AppFooter",
    data() {
        return {
            features: [
                {
                    text: "DIGITAL COMICS",
                    image: "../../public/buy-comics-digital-comics.png"
                },
                {
                    text: "DC MERCHANDISE",
                    image: "../../public/buy-comics-merchandise.png"
                },
                {
                    text: "SUBSCRIPTION",
                    image: "../../public/buy-comics-subscriptions.png"
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    image: "../../public/buy-comics-shop-locator.png"
                },
                {
                    text: "DC POWER VISA",
                    image: "../../public/buy-dc-power-visa.svg"
                },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <section class="features">
            <div class="container">
                <div v-for="feat in features" class="feat">
                    <div class="img-container">
                        <img :src="feat.image" :alt="feat.text">
                    </div>
                    <div class="feat-text">
                        {{ feat.text }}
                    </div>
                </div>
            </div>
        </section>

        <section class="info">
            <div class="container">
                <div class="col">
                    <h2>DC COMICS</h2>
                    <ul>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>

                    <h2>SHOP</h2>
                    <ul>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                </div>

                <div class="col">
                    <h2>DC</h2>
                    <ul>
                        <li><a href="#">Term Of Use</a></li>
                        <li><a href="#">Privacy policy (New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                </div>

                <div class="col">
                    <h2>SITES</h2>
                    <ul>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </div>
            </div>
        </section>

        <section class="contacts">
            <div class="container">
                <a class="button" href="#">SIGN-UP NOW!</a>
                <ul>
                    <li>
                        <h2>FOLLOW US</h2>
                    </li>
                    <li><a href="#">
                            <img src="../../public/footer-facebook.png" alt="facebook-icon">
                        </a></li>
                    <li><a href="#">
                            <img src="../../public/footer-twitter.png" alt="twitter-icon">
                        </a></li>
                    <li><a href="#">
                            <img src="../../public/footer-youtube.png" alt="youtube-icon">
                        </a></li>
                    <li><a href="#">
                            <img src="../../public/footer-facebook.png" alt="facebook-icon">
                        </a></li>
                    <li><a href="#">
                            <img src="../../public/footer-periscope.png" alt="periscope-icon">
                        </a></li>
                </ul>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;

footer {
    .features {
        background: $primary;
        color: #ffff;

        .container {
            width: 65%;
            margin: 0 auto;
            @include space();
            flex-wrap: wrap;
        }

        .feat {
            @include space();
            padding: 40px 0;
        }

        .img-container {
            width: 50px;

            img {
                width: 100%;
            }
        }

        .feat-text {
            padding-left: 12px;
            font-size: 14px;
        }
    }

    .info {
        min-height: 400px;
        background-image: url(../../public/footer-bg.jpg);
        background-size: cover;

        .container {
            width: 70%;
            margin: 0 auto;
            display: flex;
            justify-content: flex-start;
            background-image: url(../../public/dc-logo-bg.png);
            padding: 50px 0;
            background-position: right;
            background-repeat: no-repeat;
            background-size: 45%;
        }

        .col {
            color: #ffff;
            margin-right: 50px;

            h2 {
                font-size: 20px;
                margin: 10px 0;
            }

            ul {
                list-style: none;
            }

            li {
                a {
                    color: #959fa1;
                    font-size: 13px;
                    text-decoration: none;
                }
            }
        }
    }

    .contacts {
        background: #303030;
        padding: 30px 0;

        .container {
            @include space();

            .button {
                color: #ffff;
                padding: 10px 15px;
                font-size: 18px;
                border: 3px solid $primary;
                text-decoration: none;
            }

            h2 {
                color: $primary;
                font-size: 22px;
                margin-right: 10px;
            }

            ul {
                @include space();
                list-style: none;

                li {
                    margin: 0 10px;
                }
            }
        }
    }
}


// Qui ci andrà l'scss relativo al solo componente
</style>

