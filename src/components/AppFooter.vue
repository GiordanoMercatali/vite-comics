<template>
    <footer>
        <div class="upper-footer">
            <div class="row">
                <div class="col" v-for="column, indexCol in upperFooterColumns" :key="column.sectionName">
                    <h3>{{ column.sectionName }}</h3>
                    <ul>
                        <li v-for="voice, indexVoice in upperFooterColumns[indexCol].sectionVoices" :key="voice.title">
                        <a href="">{{ voice.title }}</a>
                
                        </li>
                    </ul>
                </div>

                <div class="col">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                    <!-- <img :src="getImageUrl(dc-logo-bg.png)" alt=""> -->
                </div>
            </div>

        </div>
        <div class="lower-footer">
            <div class="footer-button">
                <button class="btn btn-primary">Sign-up Now!</button>
            </div>
            <div class="logo-list">
                <h3>Follow Us</h3>
                <ul>
                    <li v-for="elem, indexElem in lowerFooterItems" :key="elem.logo" class="image-container">
                        <a href=""><img :src="getLogo(indexElem)"></a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    data(){
        return{
            upperFooterColumns: [
                {
                    sectionName: "DC Comics",
                    sectionVoices: [
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
                            title: "Videos",
                        },

                        {
                            title: "News",
                        },
                    ]
                },

                {
                    sectionName: "DC",
                    sectionVoices: [
                        {
                            title: "Terms of Use",
                            },

                        {
                            title: "Privacy policy",
                        },

                        {
                            title: "Ad Choices",
                        },

                        {
                            title: "Advertising",
                        },

                        {
                            title: "Jobs",
                        },

                        {
                            title: "Subscriptions",
                        },

                        {
                            title: "Talent Workshops",
                        },

                        {
                            title: "CPSC Certificates",
                        },

                        {
                            title: "Ratings",
                        },

                        {
                            title: "Shop Help",
                        },

                        {
                            title: "Contact Us",
                        },
                    ]
                },

                {
                    sectionName: "Sites",
                    sectionVoices: [
                        {
                            title: "DC",
                            },

                        {
                            title: "MAD Magazine",
                        },

                        {
                            title: "DC Kids",
                        },

                        {
                            title: "DC Universe",
                        },

                        {
                            title: "DC Power Visa",
                        },
                    ]
                },

                {
                    sectionName: "Shop",
                    sectionVoices: [
                        {
                            title: "Shop DC",
                            },

                        {
                            title: "Shop DC Collectibles",
                        },
                    ]
                },
            ],

            lowerFooterItems: [
                {
                    logo: '-facebook'
                },

                {
                    logo: '-periscope'
                },

                {
                    logo: '-pinterest'
                },

                {
                    logo: '-twitter'
                },

                {
                    logo: '-youtube'
                },
            ]
        }
    },

    methods: {
        getLogo: function (index) {
            return `../src/assets/img/footer${this.lowerFooterItems[index].logo}.png`;
          },

        getImageUrl: function  (imgName) {
            return new URL (`../assets/img/${imgName}`, import.meta.url).href;
        }
    },
    
}
</script>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    .upper-footer {
        background-image: url("../assets/img/footer-bg.jpg");
        background-size: cover;

            .row{
                @include flex($direction: row, $justify-content: center, $align-items: start);
                flex-wrap: wrap;
                width: 60%;
                margin: 0 auto;
                gap: 1rem;

                    h3{
                        color: white;
                        margin-bottom: .5rem;
                    }

                    li{
                        list-style-type: none;

                        a {
                            text-decoration: none;
                            color: gray;
                            font-size: 11px;
                        }
                    }
            }
    }

    .lower-footer {
        background-color: $footer-color;
        margin-top: 2rem;
        @include flex($direction: row, $justify-content: space-around, $align-items: center);

        .logo-list {     
            @include flex($direction: row, $justify-content: space-between, $align-items: center);
            gap: 1rem;      
            ul {
            @include flex($direction: row, $justify-content: space-between, $align-items: center);
            gap: 0.5rem;
            li {
                list-style-type: none;
                }
            }
        }

        
    }
</style>