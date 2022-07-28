<template>
<HeaderView logoName="Dashboard"/>
<main class="main">
  <div class="container">
    <div class="main__content">
      <div class="main__side">
        <div class="main__times">
          <!-- eslint-disable-next-line -->
          <TimesView v-for="avgTime in avgTimes"
                    :title="avgTime.title" :description="avgTime.description"/>
        </div>
        <TableView :data="data"/>
      </div>
      <div class="main__side">
        <TotalChartView/>
      </div>
    </div>
  </div>
</main>
</template>

<script>
import HeaderView from './components/HeaderView.vue';
import TimesView from './components/TimesView.vue';
import TableView from './components/TableView.vue';
import TotalChartView from './components/TotalChartView.vue';

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
      data: [
        {
          name: 'Eleanor Pena',
          project: 'Project 01',
          area: 'Finance',
          status: 'Completed',
          country: 'Australia',
        },
        {
          name: 'Savannah Nguyen',
          project: 'Project 02',
          area: 'Human Resources',
          status: 'Off track',
          country: 'Austria',
        },
        {
          name: 'Ralph Edwards',
          project: 'Project 05',
          area: 'Marketing',
          status: 'On track',
          country: 'Colombia',
        },
        {
          name: 'Eleanor Pena',
          project: 'Project 01',
          area: 'Finance',
          status: 'Completed',
          country: 'Australia',
        },
        {
          name: 'Savannah Nguyen',
          project: 'Project 02',
          area: 'Human Resources',
          status: 'Off track',
          country: 'Austria',
        },
        {
          name: 'Ralph Edwards',
          project: 'Project 05',
          area: 'Marketing',
          status: 'On track',
          country: 'Colombia',
        },
      ],
    };
  },
  components: {
    HeaderView,
    TimesView,
    TableView,
    TotalChartView,
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
