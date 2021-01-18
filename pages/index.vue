<template>
  <div>
    <div class="echarts-box">
      <h2>树状图</h2>
      <init-echarts></init-echarts>
      <h2>南丁格尔图</h2>
      <echarts-pie></echarts-pie>
    </div>
  </div>
</template>

<script>
import InitEcharts from '~/components/echarts/InitEcharts'
import EchartsPie from '~/components/echarts_pie/EchartsPie'
export default {
  name: 'index',
  data () {
    return {

    }
  },
  components: {
    InitEcharts,
    EchartsPie
  }
}
</script>
<style lang="less" scoped>
.echarts-box {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  h2 {
    margin: 20px 0;
  }
}
</style>