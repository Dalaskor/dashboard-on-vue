<template>
<div class="piechart">
    <div class="piechart__content">
        <PieChart class="piechart__chart" :width="820"/>
    </div>
</div>
</template>

<script>
import PieChart from './PieChart.vue';

export default {
  name: 'PieChartView',
  data() {
    return {
    };
  },
  props: '',
  components: {
    PieChart,
  },
};
</script>

<style scoped lang="scss">
.piechart {
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
  &__chart {}
}
</style>
