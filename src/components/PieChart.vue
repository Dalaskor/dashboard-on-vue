<template>
  <Pie
    :chart-options="chartOptions"
    :chart-data="chartData"
    :chart-id="chartId"
    :dataset-id-key="datasetIdKey"
    :plugins="plugins"
    :css-classes="cssClasses"
    :styles="styles"
    :width="width"
    :height="height"
   />
</template>

<script>
import { Pie } from 'vue-chartjs';
import {
  Chart as ChartJS, Title, Tooltip, Legend, ArcElement, CategoryScale,
} from 'chart.js';

ChartJS.register(Title, Tooltip, Legend, ArcElement, CategoryScale);

export default {
  name: 'PieChart',
  components: { Pie },
  props: {
    chartId: {
      type: String,
      default: 'pie-chart',
    },
    datasetIdKey: {
      type: String,
      default: 'label',
    },
    width: {
      type: Number,
      default: 400,
    },
    height: {
      type: Number,
      default: 400,
    },
    cssClasses: {
      default: '',
      type: String,
    },
    styles: {
      type: Object,
      default: () => {},
    },
    plugins: {
      type: Object,
      default: () => {},
    },
  },
  data() {
    return {
      chartData: {
        labels: [
          'Technology and equip...',
          'Marketing',
          'Finance',
          'Human Resources',
          'Marketing',
          'Design',
          'QA Analyst',
        ],
        datasets: [
          {
            data: [10.33, 4.19, 10.33, 4.19, 10.33, 4.19, 10.33],
            backgroundColor: ['#9747FF', '#FCA997', '#B91293', '#C3E1FF', '#FB4E22', '#F3A8E2', '#FFD7A3'],
          },
        ],
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        legend: {
          display: false,
        },
      },
    };
  },
};
</script>
