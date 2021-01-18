<template>
  <div id="pieBox"></div>
</template>
<script>
export default {
  data () {
    return {

    }
  },
  methods: {
    initCharts () {
      // 获取dom元素
      let myCharts = this.$echarts.init(document.querySelector('#pieBox'))
      // 配置表的数据
      let option = {
        backgroundColor: '#2c343c',
        name: '南丁格尔图',
        visualMap: {
          show: false,
          min: 80,
          max: 600,
          inRange: {
            colorLightness: [0, 1]
          }
        },
        series: [
          {
            name: '访问来源',
            type: 'pie',
            radius: '55%',
            data: [
              { value: 235, name: '视频广告' },
              { value: 274, name: '联盟广告' },
              { value: 310, name: '邮件营销' },
              { value: 335, name: '直接访问' },
              { value: 400, name: '搜索引擎' }
            ],
            roseType: 'angle',
            label: {
              normal: {
                textStyle: {
                  color: 'rgba(255, 255, 255, 0.3)'
                }
              }
            },
            labelLine: {
              normal: {
                lineStyle: {
                  color: 'rgba(255, 255, 255, 0.3)'
                }
              }
            },
            itemStyle: {
              normal: {
                color: '#c23531',
                shadowBlur: 200,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      }
      // 使用刚指定的配置项和数据显示图表
      myCharts.setOption(option)
    }
  },
  mounted () {
    this.initCharts()
  },
}
</script>
<style lang="less">
#pieBox {
  width: 600px;
  height: 300px;
  background-color: #eee;
}
</style>