<template>
<HeaderView logoName="Dashboard"/>
<main class="main">
  <div class="container">
    <div class="main__content">
      <div class="main__side"></div>
      <div class="main__side"></div>
    </div>
  </div>
</main>
</template>

<script>
import HeaderView from './components/HeaderView.vue';

export default {
  name: 'App',
  components: {
    HeaderView,
  },
};
</script>

<style lang="scss">
body {
  background: #011625;
}
.container {
  max-width: 1840px;
  margin: 0 auto;
}
.main {
  &__content {
    display: flex;
    align-items: start;
    justify-content: space-between;
    gap: 40px;
  }
  &__side {
    display: flex;
    flex-direction: column;
    gap: 40px;
  }
}
</style>
