<script>
export default {
    data() {
        return {
            jumbo: "src/assets/img/jumbotron.jpg"
        }
    }
}

</script>

<template>
    <section>
        <img :src="jumbo" alt="">
    </section>
</template>


<style lang="scss" scoped>
section {
    height: 400px;

    img {
        height: 100%;
        width: 100%;
        object-fit: cover;
        object-position: 20% 0;
    }
}
</style>