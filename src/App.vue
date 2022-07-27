<template>
<HeaderView logoName="Dashboard"/>
<main class="main">
  <div class="container">
    <div class="main__content">
      <div class="main__side">
        <div class="main__side-body">
          <div class="main__times">
            <!-- eslint-disable-next-line -->
            <TimesView v-for="avgTime in avgTimes"
                      :title="avgTime.title" :description="avgTime.description"/>
          </div>
        </div>
      </div>
      <div class="main__side"></div>
    </div>
  </div>
</main>
</template>

<script>
import HeaderView from './components/HeaderView.vue';
import TimesView from './components/TimesView.vue';

export default {
  name: 'App',
  data() {
    return {
      avgTimes: [
        {
          title: '23.44',
          description: 'Avq. Time To Fulfill',
        },
        {
          title: '46.24',
          description: 'Avq. Time To Fulfill',
        },
        {
          title: '34.12',
          description: 'Avq. Time To Fulfill',
        },
      ],
    };
  },
  components: {
    HeaderView,
    TimesView,
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
  &__times {
    display: flex;
    align-items: start;
    justify-content: space-between;
    gap: 40px;
  }
}
</style>
