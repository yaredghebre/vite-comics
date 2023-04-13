<script>
export default {
    name:"AppMain"
}
</script>

<template>
    <main>
        <div class="main-container container">
            <h2> --> CONTENT GOES HERE &lt;-- </h2>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    main {
        width: 100%;
        height: 200px;
        padding: 20px 0;
        background-color: $secondary_color;
        color: $fourth_color;

        .main-container {
            @include flex(row, space-between, center)
        }
    }
</style>

