<template>
  <b-container class="position-relative">
    <header class="header" :class="{ 'header--dark': theme }">
      <div>
        <router-link to="/">
          <img v-if="theme" src="~@/assets/img/everstake-logo-dark.svg" alt="Logo" />

          <img v-else src="~@/assets/img/everstake-logo-white.svg" alt="Logo" />
        </router-link>
      </div>

      <ul class="header__nav" :class="{ 'header__nav--dark': theme }">
        <li><a href="#about">About</a></li>
        <li><a href="#sector">Sectors</a></li>
        <li><a href="#advantages">Advantages</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </header>
  </b-container>
</template>

<script>
export default {
  name: 'AppHeader',
  computed: {
    theme() {
      return this.$route.path === '/form';
    },
  },
};
</script>

<style lang="scss" scoped>
.header {
  position: absolute;
  padding: 2rem 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;

  &--dark {
    position: static;
  }

  img {
    width: 50%;
  }

  &__nav {
    display: flex;
    justify-content: space-between;
    gap: 2rem;
    list-style: none;
    padding: 0;
    margin: 0;

    & a {
      color: $white;
      text-decoration: none;

      &:hover {
        color: $orange;
      }
    }

    &--dark {
      & a {
        color: $black;
      }
    }
  }
}
</style>
