<script >

    import AppMainComics from './AppMainComics.vue';

    export default {
        data() {
            return {
                contentSection: {
                    contentLinkString: 'Content goes here'
                },

                shopSection: [

                    {
                       path: '/public/img/buy-comics-digital-comics.png',
                       name: 'DIGITAL COMICS'
                    },

                    {
                      path:  '/public/img/buy-comics-merchandise.png',
                      name:  'DC MERCHANDISE'
                    },

                    {
                      path:  '/public/img/buy-comics-subscriptions.png',
                      name:  'SUBSCRIPTION'
                    },

                    {
                      path:  '/public/img/buy-comics-shop-locator.png',
                      name:  'COMIC SHOP LOCATOR'
                    },

                    {
                      path:  '/public/img/buy-dc-power-visa.svg',
                      name:  'DC POWER VISA'
                    }
                ] 
            };
        },
        components :{
            AppMainComics
        },
        methods: {

        }

    }
</script>

<template>
    <main>
        <section id="big-comic-container">
            <div id="jumbotron">
            </div>
                <AppMainComics />
        </section>
        <section id="shop">
            <ul>
                <li v-for="(shop, i) in shopSection" :key="i">
                    <div class="shop-icons">
                        <img :src="shop.path" :alt="shop.name">
                        <a href="#"> {{ shop.name }}</a>
                    </div>
                </li>
            </ul>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main';
</style>
