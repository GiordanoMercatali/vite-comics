<template lang="">
    <main>
        <h2>Content goes here</h2>
        <div class="section blue-line">
            <ul>
                    <li v-for="elem, indexElem in blueSectionItems" :key="elem.img" class="image-container">
                        <span>{{elem.img}}</span>
                        <a href=""><img :src="getImage(indexElem)"></a>
                    </li>
                </ul>
        </div>
    </main>
</template>

<script>
export default {
    data() {
        return {
            blueSectionItems: [
                {
                    img: 'comics-digital-comics'
                },

                {
                    img: 'comics-merchandise'
                },

                {
                    img: 'comics-shop-locator'
                },

                {
                    img: 'comics-subscriptions'
                },

                {
                    img: 'dc-power-visa'
                },
            ]
            
        }
    },

    methods: {
        getImage: function (index) {
            return `../src/assets/img/buy-${this.blueSectionItems[index].img}.png`;
          },
    },
}
</script>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    main{
        background-color: $main-section-color;
        color: white;

        .blue-line{
            background-color: $primary-color;
            padding: 5rem 0;

            ul {
                @include flex();
                gap: 1rem;
                li {
                    @include flex();
                    gap: 1rem;
                    img{
                        height: 50%;
                        width: 50%;
                    }
                }
            }
        }
    }
</style>