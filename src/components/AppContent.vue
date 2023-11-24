<template lang="">
    <main>
        <h2>Content goes here</h2>
        <div class="section blue-line">
            <ul>
                    <li v-for="elem, indexElem in blueSectionItems" :key="elem.img" class="image-container">
                        <span>{{elem.text}}</span>
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
                    img: 'comics-digital-comics.png',
                    text: "DIGITAL COMICS",
                },

                {
                    img: 'comics-merchandise.png',
                    text: "DC MERCHANDISE",
                },

                {
                    img: 'comics-shop-locator.png',
                    text: "COMIC SHOP LOCATOR",
                },

                {
                    img: 'comics-subscriptions.png',
                    text: "SUBSCRIPTION",
                },

                {
                    img: 'dc-power-visa.svg',
                    text: "DC POWER VISA",
                },
            ]
            
        }
    },

    methods: {
        getImage: function (index) {
            return `../src/assets/img/buy-${this.blueSectionItems[index].img}`;
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
                    
                    a {
                        img {
                        width: 50%;
                        max-width: 200px;
                    }
                    }
                }
            }
        }
    }
</style>