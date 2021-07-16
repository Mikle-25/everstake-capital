<template>
  <section class="header--wrapper">
    <b-container class="header-content pt-4 pb-5">
      <div class="header-content__middle">
        <h1 class="animated">
          Digital
          <span>age</span>
          <span>money</span>
          <span>profit</span>
        </h1>

        <p>Smarter financial decisions</p>
      </div>

      <div class="header-content__footer">
        <router-link to="/form">Get started with Everstake</router-link>
      </div>
    </b-container>
  </section>
</template>

<script>
export default {
  name: 'HomeHeader',
};
</script>

<style lang="scss" scoped>
.header--wrapper {
  background: url('../../assets/img/bgHeader.png') no-repeat;
  background-size: cover;
}

.header-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  color: $white;
  height: 100vh;

  &__middle {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100%;
    padding-left: 5rem;

    & h1 {
      font-size: $fs85;
    }

    @include xl-down {
      & h1 {
        font-size: $fs48;
      }
    }
  }

  &__footer {
    align-self: center;

    & a {
      text-decoration: none;
      padding: 1rem;
      color: $black;
      font-weight: 500;
      background-color: $white;
      transition: all 0.3s linear;

      &:hover {
        color: $white;
        background-color: $orange;
      }
    }
  }
}

.animated {
  & span {
    text-indent: 1rem;
    color: $white;
    opacity: 0;
    overflow: hidden;
    position: absolute;
    animation: animationText 9s infinite linear;
  }

  & span:nth-child(2) {
    animation-delay: 3s;
  }

  & span:nth-child(3) {
    animation-delay: 6s;
  }
}

@keyframes animationText {
  0%,
  25% {
    opacity: 0;
    transform: translateY(-50%);
  }

  35%,
  55% {
    opacity: 1;
    transform: translateY(0);
  }

  65%,
  100% {
    opacity: 0;
    transform: translateY(50%);
  }
}
</style>
