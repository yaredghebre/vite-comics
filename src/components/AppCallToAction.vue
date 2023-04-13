<script>
export default {
    name:"AppCallToAction",
    data() {
        return {
            links: {
                "DC COMICS": [
                    {
                        name: "Characters",
                        url: "#"
                    },
                    {
                        name: "Comics",
                        url: "#"
                    },
                    {
                        name: "Movies",
                        url: "#"
                    },
                    {
                        name: "TV",
                        url: "#"
                    },
                    {
                        name: "Games",
                        url: "#"
                    },
                    {
                        name: "Videos",
                        url: "#"
                    },
                    {
                        name: "News",
                        url: "#"
                    }
                ],
                "DC": [
                    {
                        name: "Terms Of Use",
                        url: "#"
                    },
                    {
                        name: "Privacy policy(New)",
                        url: "#"
                    },
                    {
                        name: "Ad Choices",
                        url: "#"
                    },
                    {
                        name: "Advertising",
                        url: "#"
                    },
                    {
                        name: "Jobs",
                        url: "#"
                    },
                    {
                        name: "Subscriptions",
                        url: "#"
                    },
                    {
                        name: "Talet Workshops",
                        url: "#"
                    },
                    {
                        name: "CPSC Certificates",
                        url: "#"
                    },
                    {
                        name: "Ratings",
                        url: "#"
                    },
                    {
                        name: "Shop Help",
                        url: "#"
                    },
                    {
                        name: "Contact Us",
                        url: "#"
                    }
                ],
                "SITES": [
                    {
                        name: "DC",
                        url: "#"
                    },
                    {
                        name: "MAD Magazine",
                        url: "#"
                    },
                    {
                        name: "DC Kids",
                        url: "#"
                    },
                    {
                        name: "DC Universe",
                        url: "#"
                    },
                    {
                        name: "DC Power Visa",
                        url: "#"
                    },
                ],
                "SHOP": [
                    {
                        name: "Shop DC",
                        url: "#"
                    },
                    {
                        name: "Shop DC Collectibles",
                        url: "#"
                    }
                ],
            },
        }
    }
}
</script>

<template>
    <section class="call-to-action">
        <div class="call-to-action-container container">
            <ul class="call-to-action-container-links">
                <li class="call-to-action-container-links-list" v-for="(elem, index) in links">
                    <h3>{{ index }}</h3>
                    <ul>
                        <li v-for="item in elem">
                            <a href="">{{ item.name }}</a>
                        </li>
                    </ul>
                </li>
            </ul>
            <img class="call-to-action-logo" src="../assets/img/dc-logo-bg.png" alt="">
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    .call-to-action {
        height: 400px;
        background-image: url(../assets/img/footer-bg.jpg);

        &-container {
            // @include flex(row, space-between, center);
            display: flex;
            color: $fourth_color;
            
            &-links {
                padding: 30px 0;
                display: flex;
                width: 100%;
                gap: 20px;

                &-list {
                    gap: 10px;
                }

                a {
                    color: grey;
                    font-size: .7rem;
               }
            }
           
            &-logo {
            object-fit: cover;
            position: relative;
            left: 65%;
            bottom: 100px;
            }
        }


        
    }
</style>

