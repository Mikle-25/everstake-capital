<template>
  <footer id="contact">
    <b-container class="d-flex flex-column align-items-center">
      <p>We are always open to dialogue. Contact our team using the email form above.</p>

      <span class="info">+372 593 56766</span>
      <span class="info">invest@everstake.capital</span>

      <div class="d-flex gap-3 mt-5 mb-1">
        <span>Terms of use</span>
        <span>Privacy police</span>
      </div>

      <span>© All Rights Reserved. Everstake Capital {{ currYear }}.</span>
    </b-container>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',
  data() {
    return {
      currYear: new Date().getFullYear(),
    };
  },
};
</script>

<style lang="scss" scoped>
footer {
  min-height: 200px;
  padding: 2rem 0;
  background-color: $black;
  color: $white;
  text-align: center;
}

.info {
  font-size: $fs24;
  font-weight: bold;
}
</style>
