<script >
    export default {
        data() {
            return {

                currentLink: 0,

                dcComics: [
                    {
                       name: 'Charachters'
                    },
                    
                    {
                        name: 'Comics'
                    },
                    {
                        name: 'Movies'
                    },
                    {
                        name: 'TV'
                    },
                    {
                        name: 'Games'
                    },
                    {
                        name: 'Videos'
                    },
                    {
                        name: 'News'
                    }
                ],

                shop: [
                    {
                        name: 'Shop DC'
                    },
                    {
                        name: 'Shop DC Collectibles'
                    }
                ],

                dc: [
                    {
                        name: 'Terms Of Use'
                    },
                    {
                        name: 'Privacy Policy (New)'
                    },
                    {
                        name: 'Ad Choices'
                    },
                    {
                        name: 'Advertising'
                    },
                    {
                        name: 'Jobs'
                    },
                    {
                        name: 'Subscription'
                    },
                    {
                        name: 'Talent Workshops'
                    },
                    {
                        name: 'CPSC Certificates'
                    },
                    {
                        name: 'Ratings'
                    },
                    {
                        name: 'Shop Help'
                    },
                    {
                        name: 'Contact Us'
                    }
                ],

                sites: [
                    {
                        name: 'DC'
                    },
                    {
                        name: 'MAD Magazine'
                    },
                    {
                        name: 'DC Kids'
                    },
                    {
                        name: 'DC Universe'
                    },
                    {
                        name: 'DC Power Visa'
                    }
                ],

                bigLogo: {
                    path: 'public/img/dc-logo-bg.png',
                    name: 'DC Logo'
                },

                button: 'SIGN-UP NOW!',

                socialLinks: [
                    'public/img/footer-facebook.png',
                    'public/img/footer-twitter.png',
                    'public/img/footer-youtube.png',
                    'public/img/footer-pinterest.png',
                    'public/img/footer-periscope.png'
                ]

            };
        },
        methods: {

        }

    }
</script>

<template>
    <footer>
        <section id="footer-top">
            <div id="footer-list-container">
                <div>
                    <h4>
                        DC COMICS
                    </h4>
                    <ul>
                        <li v-for="elem in dcComics">
                            <a href="#">
                                {{ elem.name }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h4>
                        DC
                    </h4>
                    <ul>
                        <li v-for="elem in dc">
                            <a href="#">
                                {{ elem.name }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h4>
                        SITES
                    </h4>
                    <ul>
                        <li v-for="elem in sites">
                            <a href="#">
                                {{ elem.name }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h4>
                        SHOP
                    </h4>
                    <ul>
                        <li v-for="elem in shop">
                            <a href="#">
                                {{ elem.name }}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div id="big-logo-container">
                <img :src="bigLogo.path" :alt="bigLogo.name">
            </div>
        </section>
        <section id="footer-bottom"> 
            <div id="footer-bottom-container">
                <div>
                    <button>
                        {{ button }}
                    </button>
                </div>

                <div id="social-links">
                    <span href="#">
                        FOLLOW US
                    </span>
                    <ul>
                        <li v-for="socialLink in socialLinks">
                            <a href="#">
                                <img :src="socialLink" alt="">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/footer'
</style>
