<template lang="">
    <main>

        <div class="jumbotron">
            <img src="../assets/img/jumbotron.jpg" alt="">
        </div>

        <div class="section-title">
            <h2>Product List</h2>
        </div>

        <div class="section products">
            <div class="row">
                <div class="col" v-for="(product, indexProduct) in productsList" :key="product.series">
                    <ComicCard :propThumb="product.thumb" :propPrice="product.price" :propSeries="product.series" />
                </div>
            </div>
        </div>

        <div class="section blue-line">
            <ul>
                    <li v-for="elem, indexElem in blueSectionItems" :key="elem.img" class="image-container">
                        <span>{{elem.text}}</span>
                        <a href=""><img :src="getIcons(indexElem)"></a>
                    </li>
                </ul>
        </div>
    </main>
</template>

<script>
import ComicCard from "./ComicCard.vue";

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
            ],

            productsList: [
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book"
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book"
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel"
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book"
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel"
                }
            ],            
        }
    },
    components: { ComicCard },

    methods: {
        getIcons: function (index) {
            return `../src/assets/img/buy-${this.blueSectionItems[index].img}`;
          },
    },
}
</script>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    .jumbotron{
        img {
            max-width: 100%;
        }
    }

    main{
        background-color: $main-section-color;
        color: white;

        .section-title{
            background-color: $primary-color;
            max-width: 12rem;
            padding: 1rem;
            position: relative;
            bottom: 1.5rem;
            left: 1rem;
            text-align: center;
        }

        .products{
            margin-top: 2rem;
            padding: 0 2rem;
            .row {
                @include flex();
                flex-wrap: wrap;
                gap: 4rem;
                .col {
                    .card{
                        background-color: $main-section-color;
                        text-align: center;
                        max-width: 10rem;
                    }
                }
            }
        }

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