<script >
    export default {
        data() {
            return {
                navbar: {
                    links: [
                    'CHARACTERS',
                    'COMICS',
                    'MOVIES',
                    'TV',
                    'GAMES',
                    'COLLECTIBLES',
                    'VIDEOS',
                    'FANS',
                    'NEWS',
                    'SHOP'
                    ],

                    logo: '/img/dc-logo.png'

            }


            };
        },
        methods: {

        }

    }
</script>

<template>
    <header>
        <div>
            <img :src="navbar.logo" alt="">
        </div>
        <nav id="menu">
            <ul id="menu-list">
                <li v-for="link in navbar.links">
                    <a href="#">
                        {{ link }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/header.scss';
</style>
