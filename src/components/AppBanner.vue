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
                <img :src="card.image">
                <span> {{ card.text }}</span>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    .banner-container {
        height: 200px;
        color: $fourth_color;
        background-color: $primary_color;
        @include flex(row, space-between, center);

        .banner-row {
            height: 100px;
            @include flex(row, space-between, center);

            .banner-card {
                width: 50px;
                display: flex;
                align-items: center;
                gap: 20px;
                font-size: 0.8rem;
            }
        }
    }
</style>

