<script>
export default {
    name:"AppCard",
    props: {
        title: String,
        image: String
    }
}
</script>

<template>
        <div class="card">
            <img :src="image" alt="">
            <h3>{{ title }}</h3>
        </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

        .card {
            width: calc(100% / 6 - 20px);
            height: calc(100% / 6 - 20px);
    

            img {
                height: 200px;
                width: 200px;
            }

            h2 {
                font-family: Verdana, Geneva, Tahoma, sans-serif;
                font-size: 0.7rem;
                text-align: center;
            }
    
        }
    
</style>