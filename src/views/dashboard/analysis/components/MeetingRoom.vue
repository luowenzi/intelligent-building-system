<template>
  <div class="meeting_room">
    <div class="head">
      <div class="pageTitle">
        <i></i>
        <span>设备监控</span>
      </div>
      <div class="view">
        查看
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">

</script>
<style lang="less" scoped>
.meeting_room {
  width: 400px;
  height: 270px;
  margin-top: 5px;
  background: rgba(13, 26, 57, 0.8);
  border: 1px solid #1C3762;
  box-shadow: 0px 0px 30px 0px rgba(16, 61, 115, 0.8);

  .head {
    display: flex;
    justify-content: space-between;
    align-items: center;

    .view {
      width: 60px;
      height: 32px;
      background: #144A7F;
      border-radius: 4px;
      font-size: 14px;
      font-family: Microsoft YaHei;
      font-weight: 400;
      color: #FFFFFF;
      text-align: center;
      line-height: 32px;
      cursor: pointer;
    }
  }
}
</style>