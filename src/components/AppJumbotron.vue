<script>
export default {
    name:"AppJumbotron"
}
</script>

<template>
    <section class="jumbotron">
        <div class="title-box">CURRENT SERIES</div>
    </section>
</template>

<style scope lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    .jumbotron {
        height: 400px;
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: cover;

        .title-box {
            padding: 10px;
            width: 250px;
            color: $fourth_color;
            font-size: 1.5rem;
            font-weight: 400;
            background-color: $primary_color;
            @include flex(row, space-around, center);
            position: relative;
            top: 95%;
            left: 13%;
            
        }
    }
</style>