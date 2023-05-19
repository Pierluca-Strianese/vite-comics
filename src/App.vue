<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppProducts from './components/AppProducts.vue';

export default {
    components: { AppHeader, AppProducts, AppFooter },
};
</script>

<template>
    <AppHeader />

    <main>
        <AppProducts />
    </main>

    <AppFooter />
</template>

<style scoped></style>
