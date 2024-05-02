<script>
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';


export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppBanner,
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppBanner />
  <AppFooter />
</template>

<style lang="scss"></style>