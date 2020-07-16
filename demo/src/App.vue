<template>
  <div>
   <div style="background:#fff;padding:16px 16px 0;margin-bottom:32px;">
      <line-chart :chart-data="lineChartData"/>
    </div>
    <div style="background:#fff;padding:16px 16px 0;margin-bottom:32px;">
      
      <bar-chart/>
    </div>
  </div>
</template>

<script>

import LineChart from './components/LineChart.vue'
import BarChart from './components/BarChart.vue'
const lineChartData = {
  newVisitis: {
    expectedData: [100, 120, 161, 134, 105, 160, 165],
    actualData: [120, 82, 91, 154, 162, 140, 145]
  }
}
export default {
  name: 'App',
  components: {
    BarChart,
    LineChart
  },
  data() {
    return {
      lineChartData: lineChartData.newVisitis
    }
  }
}
</script>