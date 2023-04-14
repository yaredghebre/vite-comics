<script>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppBanner from "./components/AppBanner.vue"
import AppCallToAction from "./components/AppCallToAction.vue"
import AppFooter from "./components/AppFooter.vue"

export default {
  components: {
    AppHeader,
    AppMain,
    AppBanner,
    AppCallToAction,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppBanner />
  <AppCallToAction />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss" as *;


</style>