<template>
    <header>
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>

        <nav>
            <ul>
                <li v-for="item in navItems" :key="item.title">
                <a href="">{{ item.title }}<div class="underline"></div></a>
                
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
@use "../style/partials/variables" as *;

header {
    margin-top: 2rem;
    @include flex($direction: row, $justify-content: space-around, $align-items: center);

        img{
            width: 75%;
            height: 75%;
        }
}

ul {
    @include flex();
    list-style: none;
    gap: 1rem;

    a {
        text-decoration: none;
        color: black;

        .underline{
            background-color: $primary-color;
            width: 100%;
            height: .5rem;
            position: relative;
            top: 1.7rem;
            left: 0;
            display: none;
        }

        &:hover {
            color: $primary-color;
            .underline{
                display: inline-block;
            }
        }
    }

}
    
</style>