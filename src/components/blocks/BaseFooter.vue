<template>
    <footer class="footer">
        <div class="footer_top">
            <div class="footer_top_row">
                <div v-for="(content, index) in contents" :key="index" class="col">
                    <img :src="content.url" :alt="content.alt">
                    {{content.name}}
                </div>
            </div>
        </div>
        <div class="footer_center">
            <div class="footer_center_row">
                <div class="col_left">
                    <nav class="bottom_nav">
                        <h2>dc comics</h2>
                        <ul>
                            <li><a href="#/">Characters</a></li>
                            <li><a href="#/">Comics</a></li>
                            <li><a href="#/">Movies</a></li>
                            <li><a href="#/">TV</a></li>
                            <li><a href="#/">Games</a></li>
                            <li><a href="#/">Videos</a></li>
                            <li><a href="#/">News</a></li>
                        </ul>
                    </nav>
                    <nav class="bottom_nav">
                        <h2>shop</h2>
                        <ul>
                            <li><a href="#/">Shop DC</a></li>
                            <li><a href="#/">Shop DC Collectibles</a></li>
                        </ul>
                    </nav>
                    <nav class="bottom_nav">
                        <h2>dc</h2>
                        <ul>
                            <li><a href="#/">Term Of Use</a></li>
                            <li><a href="#/">Privacy policy (New)</a></li>
                            <li><a href="#/">Ad Choice</a></li>
                            <li><a href="#/">Advertising</a></li>
                            <li><a href="#/">Jobs</a></li>
                            <li><a href="#/">Subscriprions</a></li>
                            <li><a href="#/">Talent Workshops</a></li>
                            <li><a href="#/">CPSC Certificates</a></li>
                            <li><a href="#/">Ratings</a></li>
                            <li><a href="#/">Shop Help</a></li>
                            <li><a href="#/">Contact US</a></li>
                        </ul>
                    </nav>
                    <nav class="bottom_nav">
                        <h2>sites</h2>
                        <ul>
                            <li><a href="#/">DC</a></li>
                            <li><a href="#/">MAD Magazine</a></li>
                            <li><a href="#/">DC Kids</a></li>
                            <li><a href="#/">DC Universe</a></li>
                            <li><a href="#/">DC Power Visa</a></li>
                        </ul>
                    </nav>
                </div>
                <div class="col_right">
                    <img src="../../assets/img/dc-logo-bg.png" alt="logo dc">
                </div>
            </div>
        </div>
        <div class="footer_bottom">
            <div class="footer_bottom_row">
                <div class="col_left">
                    <button class="sign_btn">Sign-up now!</button>
                </div>
                <div class="col_right">
                    <h3>Follow us</h3>
                    <a v-for="(social, index) in socials" :key="index" href="#/"><img :src="social.url" :alt="social.name"></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'BaseFooter',
    data() {
        return {
            contents: [
                {
                    name: 'digital comics',
                    url: require('../../assets/img/buy-comics-digital-comics.png'),
                    alt: 'digital comics',
                },
                {
                    name: 'dc merchandise',
                    url: require('../../assets/img/buy-comics-merchandise.png'),
                    alt: 'dc merchandise',
                },
                {
                    name: 'subscription',
                    url: require('../../assets/img/buy-comics-subscriptions.png'),
                    alt: 'subscription',
                },
                {
                    name: 'comic shop locator',
                    url: require('../../assets/img/buy-comics-shop-locator.png'),
                    alt: 'shop locator',
                },
                {
                    name: 'dc power visa',
                    url: require('../../assets/img/buy-dc-power-visa.svg'),
                    alt: 'dc power visa',
                },
            ],
            socials: [
                {
                    name: 'facebook',
                    url: require('../../assets/img/footer-facebook.png')
                },
                {
                    name: 'twitter',
                    url: require('../../assets/img/footer-twitter.png')
                },
                {
                    name: 'youtube',
                    url: require('../../assets/img/footer-youtube.png')
                },
                {
                    name: 'pinterest',
                    url: require('../../assets/img/footer-pinterest.png')
                },
                {
                    name: 'periscope',
                    url: require('../../assets/img/footer-periscope.png')
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/mixins.scss';
.footer {

    &_top{
        
        padding: 2.5rem;
        background-color: var(--primary-color);

        &_row {
            @include flex ('between', 'center');
            width: var(--container-lg);
            margin: var(--margin-auto);
            gap: 0.5rem;

            .col {
            width: calc(100% / 5 - 0.5rem);
            color: var(--text-white);
            text-transform: uppercase;
            font-size: var(--font-sm);
            text-align: center;

                img {
                    height: 3rem;
                    vertical-align: middle;
                    object-fit: contain;
                    margin-right: 0.5rem;

                    &:last-child {
                        width: 3rem;
                    }
                }
            }
        }
    }

    &_center {
        background-image: url("../../assets/img/footer-bg.jpg");
        background-repeat: no-repeat;
        background-size: cover;

        &_row {
            @include flex('between', 'center');
            max-width: var(--container-lg);
            margin: var(--margin-auto);
            max-height: 300px;
            overflow: hidden;

            .col_left {
                display: flex;
                flex-direction: column;
                color: #859595;
                font-size: 0.8rem;
                font-weight: 100;
                gap: 0.5rem;
                flex-wrap: wrap;
                max-height: 300px;
                margin: 2.5rem 0;

                nav {
                    padding-right: 0.8rem;
                }

                h2 {
                color: var(--text-white);
                text-transform: uppercase;
                margin-bottom: 0.5rem;
                }

                ul {
                list-style: none;

                    li {
                        padding: 0.1rem 0;
                    }
                }

                a {
                    text-decoration: none;
                    color: inherit;
                }
            }
            
        }
    }

    &_bottom {
        background-color: var(--secondary-color);

        &_row {
            @include flex('between', 'center');
            max-width: var(--container-lg);
            margin: var(--margin-auto);
            padding: 2.5rem 0;
        }

        .sign_btn {
            text-transform: uppercase;
            color: var(--text-white);
            border: 0.125rem solid var(--primary-color);
            padding: 0.5rem;
            background-color: transparent;
        }

        .col_right {
            text-align: right;
            @include flex ('center', 'center');
            gap: 1rem;

            h3 {
                color: var(--primary-color);
                text-transform: uppercase;
            }
        }

    }
}
</style>