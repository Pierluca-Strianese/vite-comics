<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/appHeader.vue';
import AppProducts from './components/AppProducts.vue';
import AppJumbo from './components/AppJumbo.vue'

export default {
    components: { AppHeader, AppProducts, AppFooter, AppJumbo },
};
</script>

<template>
    <AppHeader />
    <AppJumbo />

    <main>
        <AppProducts />
    </main>

    <AppFooter />
</template>

<style lang="scss">
@import "bootstrap/scss/bootstrap";
</style>
