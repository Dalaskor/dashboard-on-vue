<template>
<div class="totalchart">
    <div class="totalchart__content">
        <BarChart class="totalchart__chart" :width="820"/>
    </div>
</div>
</template>

<script>
import BarChart from './BarChart.vue';

export default {
  name: 'TotalChartView',
  data() {
    return {
    };
  },
  props: '',
  components: {
    BarChart,
  },
};
</script>

<style scoped lang="scss">
.totalchart {
  &__content {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 900px;
    height: 496px;
    background: #001D31;
    border: 1px solid #36434E;
    border-radius: 8px;
  }
  &__chart {
    font-family: 'Inter';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: #FFFFFF;
  }
}
</style>
