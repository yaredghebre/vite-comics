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
                    img: "footer-twitter.png",
                    url: "#"
                },
                {
                    img: "footer-youtube.png",
                    url: "#"
                },
                {
                    img: "footer-pinterest.png",
                    url: "#"
                },
                {
                    img: "footer-periscope.png",
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
                <a href="">SIGN-UP NOW!</a>
                <div class="footer-container-button-icons">
                    <a href="">FOLLOW US!</a>
                    <ul>
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
        height: 500px;
        padding: 20px 0;
        background-color: $third_color;

        .footer-container {
            @include flex(row, space-between, center);

            &-button {
                width: 100%;
                @include flex(row, space-between, center);
            }

        }
    }
    
</style>

