<template>
  <div>
    <AppHeader />
    <AppMain />
    <AppNavbar />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppNavbar from './components/AppNavbar.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppNavbar,
    AppFooter
  }
}
</script>

<style lang="scss">
  @use './styles/general' as *;
</style>