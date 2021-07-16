<template>
  <div id="app">
    <AppHeader />

    <router-view />

    <AppFooter />
  </div>
</template>

<script>
import AppHeader from '@/components/app/AppHeader.vue';
import AppFooter from '@/components/app/AppFooter.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
  },
};
</script>

<style lang="scss">
@import 'assets/scss/index';

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: 'Roboto', sans-serif;
  font-size: $fs18;
}
</style>
