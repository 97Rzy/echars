<template>
  <div class="echarts-box">
    <h2>树状图</h2>
    <init-echarts></init-echarts>
    <h2>南丁格尔图</h2>
    <echarts-pie></echarts-pie>
    <h2>饼状图</h2>
    <echarts-circle></echarts-circle>
  </div>
</template>

<script>
import InitEcharts from '~/components/echarts/InitEcharts'
import EchartsPie from '~/components/echarts_pie/EchartsPie'
import EchartsCircle from '~/components/echarts_circle/EchartsCircle'
export default {
  name: 'index',
  data () {
    return {

    }
  },
  components: {
    InitEcharts,
    EchartsPie,
    EchartsCircle
  }
}
</script>
<style lang="less" scoped>
.echarts-box {
  position: absolute;
  left: 50%;
  transform: translate(-50%, 0%);
  h2 {
    margin: 20px 0;
  }
}
</style>