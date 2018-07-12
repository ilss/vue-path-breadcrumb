<template>
  <div>
    <!-- 语言切换 -->
    <sedu-echarts domId="aaaa"
                  :option=option1 />
    <sedu-echarts domId="bbb"
                  :option=option1 />
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      option1: {}
    }
  },
  created(){
    setTimeout(() => {
      this.option1 = {
        title: { text: "ECharts Gauge" },
        tooltip: { formatter: "{a} <br/>{b} : {c}%" },
        series: [
          {
            name: "业务指标",
            type: "gauge",
            detail: { formatter: "{value}%" },
            data: [{ value: 50 }]
          }
        ]
      };
      }, 3000);
  }
}
</script>

