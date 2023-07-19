<template>
  <div class="header">
    <div class="time">
      <img src="/@/assets/images/time.png" alt="" />
      <span>2020-12-25 13:08:29 星期五 晴</span>
    </div>
    <div class="title">
      <img src="/@/assets/images/LOGO1.png" alt="" />
      <span>XXX智能建筑集成平台</span>
    </div>
    <div class="tabs">
      <ul>
        <li>
          <img src="/@/assets/images/2d_icon.png" alt="" />
          <span>2D</span>
        </li>
        <li>
          <img src="/@/assets/images/3d_icon.png" alt="" />
          <span>3D</span>
        </li>
        <li>
          <img src="/@/assets/images/earth_icon.png" alt="" />
          <span>地图</span>
        </li>
        <li>
          <img src="/@/assets/images/skin_icon.png" alt="" />
          <span>换肤</span>
        </li>
      </ul>
    </div>
  </div>
</template>
<script setup lang="ts"></script>
<style lang="less" scoped>
  .header {
    width: 100%;
    height: 60px;
    background: url('/@/assets/images/logo_bg.png') top left no-repeat;
    background-size: 100% 100%;
    position: relative;

    .time {
      display: flex;
      justify-content: center;
      align-items: center;
      position: absolute;
      left: 210px;
      top: 20px;

      img {
        width: 16px;
        height: 16px;
        border-radius: 50%;
        margin-right: 6px;
      }

      span {
        font-size: 14px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #b4e6ff;
        line-height: 26px;
      }
    }

    .title {
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;

      img {
        width: 100px;
        height: 60px;
      }

      span {
        font-size: 22px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #b4e6ff;
        line-height: 24px;
      }
    }

    .tabs {
      position: absolute;
      right: 163px;
      top: 20px;

      ul {
        list-style: none;
        display: flex;
        align-items: center;

        li {
          display: flex;
          align-items: center;
          margin-left: 18px;
          padding: 6px 9px;
          background: rgba(51, 95, 161, 0.3);
          border-radius: 4px;
          img {
            width: 14px;
            height: 14px;
            margin-right: 5px;
          }
          span {
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #b4e6ff;
            line-height: 17px;
          }
        }
      }
    }
  }
</style>
