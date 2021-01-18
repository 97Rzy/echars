<template>
  <div id="myEchars"></div>
</template>
<script>
export default {
  data () {
    return {
    }
  },
  methods: {
    echartsInit () {
      // 基于准备好的dom，初始化echarts实例
      let eCharts = this.$echarts.init(document.getElementById('myEchars'))
      // 指定图表的配置项和数据
      var option = {
        // echarts的标题
        title: {
          text: 'ECharts 入门示例'
        },
        tooltip: {},
        legend: {
          data: ['销量']
        },
        // x轴的名称
        xAxis: {
          data: ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"]
        },
        yAxis: {},
        // 设置echarts的类型,以及显示的数据
        series: [{
          name: '销量',
          type: 'bar',
          data: [5, 20, 36, 10, 10, 20]
        }]
      };
      // 使用刚指定的配置项和数据显示图表。
      eCharts.setOption(option);
    }
  },
  mounted () {
    this.echartsInit()
  },
}
</script>
<style lang="less">
#myEchars {
  width: 600px;
  height: 300px;
  background-color: #eee;
}
</style>