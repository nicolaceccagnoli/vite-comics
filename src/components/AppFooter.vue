<script >
    export default {
        data() {
            return {
                footerTopLists: [
                    {
                        title: 'DC COMICS',
                        links: [
                            'Characters',
                            'Comics',
                            'Movies',
                            'TV',
                            'Games',
                            'Videos',
                            'News'
                        ]
                    },
                    {
                        title: 'SHOP',
                        links: [
                            'Shop DC',
                            'Shop DC Collectibles'
                        ]
                    },
                    {
                        title: 'DC',
                        links: [
                            'Terms Of Use',
                            'Privacy policiy (New)',
                            'Ad Choices',
                            'Advertising',
                            'Jobs',
                            'Subscriptions',
                            'Talent Workshops',
                            'CPSC Certificates',
                            'Ratings',
                            'Shop Help',
                            'Contact Us'
                        ]
                    },
                    {
                        title: 'SITES',
                        links: [
                            'DC',
                            'MAD Magazine',
                            'DC Kids',
                            'DC Universe',
                            'DC Power Visa'
                        ]
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
                <div v-for="list in footerTopLists">
                    <h4>
                        {{ list.title }}
                    </h4>
                    <ul>
                        <li v-for="(link, i) in footerTopLists.links">
                            <a href="#">
                                {{ footerTopLists.links[i].link[activeLink] }}
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
