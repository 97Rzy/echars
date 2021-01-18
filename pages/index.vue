<template>
  <div>
    <div class="echarts-box">
      <h1>echars学习</h1>
      <init-echarts></init-echarts>
    </div>
  </div>
</template>

<script>
import InitEcharts from '~/components/echarts/InitEcharts'
export default {
  name: 'index',
  data () {
    return {

    }
  },
  components: {
    InitEcharts
  }
}
</script>
<style lang="less" scoped>
.echarts-box {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  h1 {
    margin-bottom: 50px;
  }
}
</style>