<template>
  <div class="home">
    <HomeHeader />
    <HomeBody />
  </div>
</template>

<script>
// @ is an alias to /src
import HomeHeader from '@/components/home/HomeHeader.vue';
import HomeBody from '@/components/home/HomeBody.vue';

export default {
  name: 'Home',
  components: {
    HomeBody,
    HomeHeader,
  },
};
</script>

<style lang="scss">
.home {
  width: 100%;
}
</style>
