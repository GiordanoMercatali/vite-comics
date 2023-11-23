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
            </div>

            <div class="row">
            </div>

        </div>
        <div class="lower-footer">
            addio
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
            ]
        }
    }
    
}
</script>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;

    .upper-footer {
        background-image: url("../assets/img/footer-bg.jpg");

            .row{
                @include flex($direction: row, $justify-content: space-around, $align-items: start);
                flex-wrap: wrap;
                width: 50%;

                    h3{
                        color: white;
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
        background-color: gray;
    }
</style>