<script>
import ListIcons from './components/ListIcons.vue';
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';


export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    ListIcons,
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <ListIcons />
  <AppFooter />
</template>

<style lang="scss"></style>