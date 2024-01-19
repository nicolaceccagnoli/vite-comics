<script >
    export default {
        data() {
            return {

            links: [

                    {
                        name: 'CHARACTERS',
                        link: '#',
                        active: false
                    },
                    {
                        name: 'COMICS',
                        link: '#',
                        active: true
                    },
                    {
                        name: 'MOVIES',
                        link: '#',
                        active: false
                    },
                    {
                        name: 'TV',
                        link: '#',
                        active: false
                    },
                    {
                        name: 'GAMES',
                        link: '#',
                        active: false
                    },
                    {
                        name: 'COLLECTIBLES',
                        link: '#',
                        active: false
                    },
                    {
                        name: 'VIDEOS',
                        link: '#',
                        active: false
                    },
                    {
                        name: 'FANS',
                        link: '#',
                        active: false
                    },
                    {
                        name: 'NEWS',
                        link: '#',
                        active: false
                    },
                    {
                        name: 'SHOP',
                        link: '#',
                        active: false
                    }

                    ],

                    logo: '/img/dc-logo.png'

            };
        },
        
        methods: {

        }

    }
</script>

<template>
    <header>
        <div>
            <img :src="logo" alt="">
        </div>
        <nav id="menu">
            <ul id="menu-list">
                <li v-for="(link, i) in links" :key="i">
                    <a :class="{
                        'active' : links[i].active
                    }" href="#">
                        {{ links[i].name }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/header';
</style>
