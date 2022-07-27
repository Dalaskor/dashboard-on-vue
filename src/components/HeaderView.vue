<template>
  <header class="header">
    <div class="container">
      <div class="header__content">
        <h1 class="header__logo">{{ logoName }}</h1>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderView',
  props: {
    logoName: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
  &__content {
    display: flex;
    align-items: center;
    justify-content: start;
    padding: 40px 0px;
  }
  &__logo {
    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 36px;
    line-height: 48px;
    color: #fff;
    margin: 0;
  }
}
</style>
