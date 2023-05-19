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
    <nav>
        <ul>
            <li v-for="menuItem in menuData" :key="menuItem.name" class="active">
                <a :href="menuItem.src">{{ menuItem.name }}</a>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss" scoped>
ul {
    display: flex;
    list-style-type: none;

    li {
        padding: 1rem;
    }

    .active {
        color: blue;
        border-bottom: 7px solid blue;

    }

    a {
        text-decoration: none;
    }
}
</style>