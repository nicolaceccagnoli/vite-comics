<script >
    export default {
        data() {
            return {

            };
        },
        props: {
            path: String,
            currentSeries: String,
        }

    }
</script>

<template>
    <div class="single-comic">
        <div>
            <img :src="path" :alt="currentSeries">
        </div>

        <h3>
            {{ currentSeries }}
        </h3>
    </div>
</template>

<style lang="scss" scoped>
    @use '../assets/scss/main';
</style>
