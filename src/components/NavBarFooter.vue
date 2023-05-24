<script>
export default {
    data() {
        return {
            items: [
                {
                    img: "buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS",
                    url: "#"
                },
                {
                    img: "buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url: "#"
                },
                {
                    img: "buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url: "#"
                },
                {
                    img: "buy-comics-shop-locator.png",
                    text: "COMIC CHOP LOCATOR",
                    url: "#"
                },
                {
                    img: "buy-dc-power-visa.svg",
                    text: "DC POWER VISA",
                    url: "#"
                }
            ]
        }
    },

    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },
    },
}

</script>

<template>
    <section class="merchandise">
        <ul class="container">
            <li v-for="item in items">
                <img :src="getImagePath(item.img)" alt="">
                <a :href="item.url">{{ item.text }}</a>
            </li>
        </ul>
    </section>
</template>


<style lang="scss" scoped>
@use "../style/general.scss" as *;

.merchandise {
    background-color: $primary;
    height: 125px;

    .container {
        display: flex;
        justify-content: center;
        height: 100%;
        padding: 10px 40px;

        li {
            display: flex;
            justify-content: center;
            align-items: center;
            padding-inline: 10px;

            a {
                padding-left: 5px;
                color: $text-white;
                text-decoration: none;
                font-size: .8rem;
            }

            img {
                height: 40px;
            }
        }
    }
}
</style>