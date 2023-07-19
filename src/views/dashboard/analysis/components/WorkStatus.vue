<template>
  <div class="work_status">
    <div class="pageTitle">
      <i></i>
      <span>设备监控</span>
    </div>
    <div class="content">
      <div class="workEch" ref="workEch"></div>
    </div>
  </div>
</template>
<script setup lang="ts">
  import { Ref, ref, watch } from 'vue';
  import { useECharts } from '/@/hooks/web/useECharts';
  const workEch = ref<HTMLDivElement | null>(null);
  const { setOptions } = useECharts(workEch as Ref<HTMLDivElement>);
  watch(
    () => {
      setOptions({
        tooltip: {
          trigger: 'axis',
          axisPointer: {
            // Use axis to trigger tooltip
            type: 'shadow', // 'shadow' as default; can also be 'line' or 'shadow'
          },
        },
        legend: {},
        grid: {
          left: '3%',
          right: '4%',
          bottom: '5%',
          containLabel: true,
        },
        xAxis: {
          type: 'value',
          show: false,
        },
        yAxis: {
          type: 'category',
          data: ['今年', '累计'],
        },
        series: [
          {
            name: '今年',
            type: 'bar',
            stack: 'total',
            label: {
              show: true,
            },
            emphasis: {
              focus: 'series',
            },
            data: [150, 212],
          },
          {
            name: '去年',
            type: 'bar',
            stack: 'total',
            label: {
              show: true,
            },
            emphasis: {
              focus: 'series',
            },
            data: [820, 832],
          },
        ],
      });
    },
    { immediate: true },
  );
  // option && myChart.setOption(option);
</script>
<style lang="less">
  .work_status {
    width: 400px;
    height: 220px;
    background: rgba(13, 26, 57, 0.8);
    border: 1px solid #1c3762;
    box-shadow: 0px 0px 30px 0px rgba(16, 61, 115, 0.8);

    .content {
      width: 100%;
      height: 200px;

      .workEch {
        width: 100%;
        height: 200px;
      }
    }
  }
  .pageTitle {
    margin-top: 7px;
    width: 115px;
    height: 32px;
    background: linear-gradient(90deg, #0c1a38 0%, #144a7f 68%, #0e2a54 93%);
    display: flex;
    align-items: center;
    color: #b4e6ff;
    i {
      display: inline-block;
      width: 3px;
      height: 16px;
      background: #b4e6ff;
      margin: 0 8px 0 14px;
    }
  }
</style>
