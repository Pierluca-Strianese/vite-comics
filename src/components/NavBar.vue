<script>
export default {
    data() {
        return {
            menuData: [
                {
                    name: 'CHARACTERS',
                    src: '#',
                    active: false,
                },
                {
                    name: 'COMICS',
                    src: '#',
                    active: false,
                },
                {
                    name: 'MOVIES',
                    src: '#',
                    active: false,
                },
                {
                    name: 'TV',
                    src: '#',
                    active: false,
                },
                {
                    name: 'GAMES',
                    src: '#',
                    active: false,
                },
                {
                    name: 'COLLECTIBLES',
                    src: '#',
                    active: false,
                },
                {
                    name: 'VIDEO',
                    src: '#',
                    active: false,
                },
                {
                    name: 'FANS',
                    src: '#',
                    active: false,
                },
                {
                    name: 'NEWS',
                    src: '#',
                    active: false,
                },
                {
                    name: 'SHOP',
                    src: '#',
                    active: false,
                },
            ],
        };
    },
};
</script>

<template>
    <div>
        <ul>
            <li v-for="menuItem in menuData" :key="menuItem.name" class="active">
                <a :href="menuItem.src">{{ menuItem.name }}</a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
div {
    height: 100%;
}

ul {
    display: flex;
    list-style-type: none;
    margin: 0;
    height: 100%;

    li {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 1rem;
        font-size: .8rem;
    }

    .active {
        color: blue;
        border-bottom: 5px solid blue;

    }

    a {
        text-decoration: none;
    }
}
</style>