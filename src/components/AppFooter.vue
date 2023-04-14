<script>
export default {
    name:"AppFooter",
    data() {
        return {
            icons: [
                {
                    img: "src/assets/img/footer-facebook.png",
                    url: "#"
                },
                {
                    img: "src/assets/img/footer-twitter.png",
                    url: "#"
                },
                {
                    img: "src/assets/img/footer-youtube.png",
                    url: "#"
                },
                {
                    img: "src/assets/img/footer-pinterest.png",
                    url: "#"
                },
                {
                    img: "src/assets/img/footer-periscope.png",
                    url: "#"
                },
            ]
        }
    },
    // methods: {
    //     getImgPath(name) {
    //         return `../assets/img/${name.img}`;
    //     }
    // }
}
</script>

<template>
    <footer>
        <div class="footer-container container">
            <div class="footer-container-button">
                <div class="sign-up-btn">
                    <a href="">SIGN-UP NOW!</a>
                </div>
                <div class="footer-container-button-icons">
                    <a href="">FOLLOW US!</a>
                    <ul class="list">
                        <li v-for="icon in icons">
                            <a :href="icon.url">
                                <img :src="icon.img" alt="">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>

            <!-- <ul>
                <li>
                    <a href="">FOLLOW US</a>
                </li>
                <li v-for="icon in icons">
                    <a :href="icon.url">
                        <img :src="getImgPath(icon)" alt="">
                    </a>
                </li>
            </ul> -->
            
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    footer {
        width: 100%;
        padding: 20px 0;
        background-color: rgba(0, 0, 0, 0.743);

        .footer-container {
            @include flex(row, space-between, center);
            // z-index: 100;
            // position: relative;

            &-button {
                width: 100%;
                @include flex(row, space-between, center);
                color: white;

                .sign-up-btn {
                    border: 2px solid $primary_color;
                    padding: 5px;
                }

                &-icons {
                    @include flex(row, space-between, center);
                    color: $primary_color;
                    gap: 20px;

                    .list {
                        display: flex;
                        gap: 20px;
                    }
                }
            }

        }
    }
    
</style>

