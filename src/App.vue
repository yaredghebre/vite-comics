<script>
import AppHeader from "./components/AppHeader.vue"
import AppJumbotron from "./components/AppJumbotron.vue"
import AppMain from "./components/AppMain.vue"
import AppBanner from "./components/AppBanner.vue"
import AppCallToAction from "./components/AppCallToAction.vue"
import AppFooter from "./components/AppFooter.vue"

export default {
  components: {
    AppHeader,
    AppJumbotron,
    AppMain,
    AppBanner,
    AppCallToAction,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader />
  <AppJumbotron />
  <AppMain />
  <AppBanner />
  <AppCallToAction />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss" as *;


</style>