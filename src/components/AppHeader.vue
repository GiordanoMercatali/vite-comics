<template>
    <header>
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>

        <nav>
            <ul>
                <li v-for="item in navItems" :key="item.title">
                <a href="">{{ item.title }}</a>
            </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    data(){
        return{
            navItems: [
                {
                    title: "Characters",
                },

                {
                    title: "Comics",
                },

                {
                    title: "Movies",
                },

                {
                    title: "TV",
                },

                {
                    title: "Games",
                },

                {
                    title: "Collectibles",
                },

                {
                    title: "Videos",
                },

                {
                    title: "Fans",
                },

                {
                    title: "News",
                },

                {
                    title: "Shop",
                },
            ]
        }
    }
    
}
</script>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;

header {
    margin-top: 2rem;
    @include flex($direction: row, $justify-content: space-around, $align-items: center);
}

ul {
    @include flex();
    list-style: none;
    gap: 1rem;

    a {
        text-decoration: none;
        color: black;

        &:hover {
        color: blue;
        }
    }

}
    
</style>