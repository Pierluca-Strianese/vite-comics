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
            <li v-for="(menuItem, i) in menuData" :key="i">
                <a :href="menuItem.src" :class="{ active: menuItem.active }">{{ menuItem.name }}</a>
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
    justify-content: center;
    align-items: center;
    list-style-type: none;
    margin: 0;
    height: 100%;

    li {
        display: flex;
        padding-inline: 15px;
        height: 100%;
        align-items: center;

        &:hover,
        &.active {
            border-bottom: 4px solid blue;
            cursor: pointer;
        }

        a {
            color: black;
            text-decoration: none;
        }
    }
}
</style>