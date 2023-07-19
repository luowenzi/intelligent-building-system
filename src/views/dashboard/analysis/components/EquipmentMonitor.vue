<template>
  <div class="equipmentMonitor">
    <div class="pageTitle">
      <i></i>
      <span>设备监控</span>
    </div>
    <div class="content">
      <div class="total">
        <div class="device">
          <span> 设备总数 </span>
          <span> 150 </span>
        </div>
        <div class="callP">
          <span>报警数量</span>
          <span>36</span>
        </div>
      </div>
    </div>
    <canvas id="myCanvas"></canvas>
    <img style="display: none" id="scream" :src="img" />
  </div>
</template>
<script lang="ts" setup>
  import { onMounted } from 'vue';
  import img from '/@/assets/images/canvasData.jpg';
  // 绘制图表
  onMounted(() => {
    setTimeout(() => {
      const c = document.getElementById('myCanvas') as HTMLCanvasElement;
      const ctx = c.getContext('2d')!;
      const scream = document.getElementById('scream') as HTMLImageElement;
      ctx.drawImage(scream, 0, 0, 300, 100);
    }, 1000);
  });
</script>
<style lang="less" scoped>
  .equipmentMonitor {
    margin-top: 5px;
    width: 400px;
    height: 268px;
    background: rgba(13, 26, 57, 0.8);
    border: 1px solid #1c3762;
    box-shadow: 0px 0px 30px 0px rgba(16, 61, 115, 0.8);

    .content {
      padding: 0 20px;
      margin-top: 4px;

      .total {
        width: 360px;
        height: 40px;
        background: rgba(0, 0, 0, 0.12);
        border: 1px solid #2451a4;
        border-top: none;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 20px;

        .device {
          width: 50%;
          border-right: 1px solid linear-gradient(0deg, #1c245c 0%, #2451a4 100%);
          text-align: center;
          vertical-align: middle;

          span:first-child {
            font-size: 16px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            line-height: 19px;
            margin-right: 12px;
          }

          span:last-child {
            font-size: 24px;
            font-family: 300-CAI978;
            color: #15b1ff;
            line-height: 19px;
          }
        }

        .callP {
          width: 50%;
          border-right: 1px solid linear-gradient(0deg, #1c245c 0%, #2451a4 100%);
          text-align: center;
          vertical-align: middle;

          span:first-child {
            font-size: 16px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            line-height: 19px;
            margin-right: 12px;
          }

          span:last-child {
            font-size: 24px;
            font-family: 300-CAI978;
            color: #ff0000;
            line-height: 19px;
          }
        }
      }
    }
  }
</style>
<style lang="less">
  canvas {
    margin-top: 20px;
    margin-left: 20px;
    width: 360px;
  }
</style>
