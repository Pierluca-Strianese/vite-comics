<script>
export default {
    props: {
        thumb: Object
    }
}

</script>

<template>
    <div class="card">
        <div>
            <img :src="thumb.thumb" :alt="thumb.series">
        </div>
        <h4>{{ thumb.series }}</h4>
    </div>
</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 30px);
    margin: 20px 15px;
    background-color: black;

    img {
        width: 100%;
        aspect-ratio: 3 / 4;
    }

    h4 {
        margin-top: 10px;
        padding-left: 5px;
        font-size: 1rem;
        text-align: left;
        color: white;
    }
}
</style>