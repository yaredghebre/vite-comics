<script>
export default {
    name:"AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <nav class="header-menu container">
            <div class="header-logo-box">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>
            <ul class="header-links">
                <li v-for="link in links" :class="link.current ? 'active' : ''">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

    header {
        width: 100%;
        height: 100px;
        display: flex;
        .header-menu {
            @include flex(row, space-between, center)
        }

        .header-logo-box {
            // width: 30%;
            width: 70px;
            height: 70px;
        }

        .header-links {
            width: 70%;
            display: flex;
            align-items: end;
            gap: 50px;

            li {
                
                a:hover:after {
                    content: "";
                    display: block;
                    height: 5px;
                    background-color: $primary_color;
                    position: relative;
                    top: 35px;
                }

                &.active,
                &:hover {
                    color: $primary_color;
                }
            }
        }
    }


</style>

