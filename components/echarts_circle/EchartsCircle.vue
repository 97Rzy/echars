<template>
  <div id="Charts"></div>
</template>
<script>
export default {
  name: "EchartsCircle",
  data () {
    return {

    }
  },
  methods: {
    initCharts () {
      let myCharts = this.$echarts.init(document.querySelector('#Charts'))
      let option = {
        title: {
          text: "饼状图",
        },
        series: [
          {
            name: '访问来源',
            type: 'pie',
            radius: '55%',
            data: [
              { value: 235, name: '视频广告', itemStyle: { color: '#f39c12' } },
              { value: 274, name: '联盟广告', itemStyle: { color: '#9b59b6' } },
              { value: 310, name: '邮件营销', itemStyle: { color: '#e74c3c' } },
              { value: 335, name: '直接访问', itemStyle: { color: '#1abc9c' } },
              { value: 400, name: '搜索引擎', itemStyle: { color: '#3498db' } }
            ]
          }
        ]
      }
      myCharts.setOption(option)
    }
  },
  mounted () {
    this.initCharts()
  },
}
</script>
<style lang="less">
#Charts {
  width: 600px;
  height: 300px;
  background-color: #eeeeee;
}
</style>