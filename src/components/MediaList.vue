<template>
  <div class="media">
    <a href=""><img src="~@/assets/img/media-icon/tw.svg" alt="twitter"/></a>
    <a href=""><img src="~@/assets/img/media-icon/in.svg" alt="linkedin"/></a>
    <a href=""><img src="~@/assets/img/media-icon/mail.svg" alt="mail"/></a>
    <a href=""><img src="~@/assets/img/media-icon/tm.svg" alt="telegram"/></a>
  </div>
</template>

<script>
export default {
  name: 'MediaList',
};
</script>

<style lang="scss" scoped>
.media {
  display: flex;
  justify-content: center;
  column-gap: 1rem;
  margin: 5rem 0 2rem;
}
</style>
