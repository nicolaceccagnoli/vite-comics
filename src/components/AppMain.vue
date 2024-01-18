<script >
    export default {
        data() {
            return {
                contentLinkString: 'Content goes here',
            };
        },
        methods: {

        }

    }
</script>

<template>
    <main>
        <section id="content">
            <a href="#">
                <i class="fa-solid fa-arrow-right-long"></i>
                    {{ contentLinkString }} 
                <i class="fa-solid fa-arrow-left-long"></i>
            </a>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main'
</style>
