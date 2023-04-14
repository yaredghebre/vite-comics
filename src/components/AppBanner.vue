<script>
export default {
    name:"AppBanner",
    data() {
        return {
            cards: [
                {
                    image:"src/assets/img/buy-comics-digital-comics.png",
                    text:"DIGITAL COMICS"
                },
                {
                    image:"src/assets/img/buy-comics-merchandise.png",
                    text:"DC MERCHANDISE"
                },
                {
                    image:"src/assets/img/buy-comics-subscriptions.png",
                    text:"SUBSCRIPTION"
                },
                {
                    image:"src/assets/img/buy-comics-shop-locator.png",
                    text:"COMIC SHOP LOCATION"
                },
                {
                    image:"src/assets/img/buy-dc-power-visa.svg",
                    text:"DC POWER VISA"
                },
            ]

        }
    }
}
</script>

<template>
    <section class="banner-container ">
        <div class="banner-row container">
            <div class="banner-card" v-for="card in cards">
                <div class="banner-box">
                    <img :src="card.image">
                </div>
                
                <span> {{ card.text }}</span>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    .banner-container {
        height: 100px;
        color: $fourth_color;
        background-color: $primary_color;
        @include flex(row, space-between, center);
        z-index: 100;
        position: relative;

        .banner-row {
            height: 100px;
            @include flex(row, space-between, center);

            .banner-card {
                // width: 50px;
                display: flex;
                align-items: center;
                gap: 10px;
                font-size: 0.8rem;

                .banner-box {
                    width: 50px;
                    height: 50px;

                    img {
                        height: 100%;
                        max-width: 100%;
                    }
                }
            }
        }
    }
</style>

