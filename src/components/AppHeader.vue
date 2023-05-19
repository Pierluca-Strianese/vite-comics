<script>
import NavBar from './NavBar.vue';

export default {
    data() {
        return {
            logoImgName: 'dc-logo.png',
        };
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },
    },
    components: {
        NavBar,
    },
}
</script>

<template>
    <header>
        <div class="container">
            <img :src="getImagePath(logoImgName)" alt="" />
            <NavBar />
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100px;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;

        img {
            height: 5rem;
            aspect-ratio: 1 / 1;
        }
    }
}
</style>