<template>
  <div class="dialog">
    <div class="staging">
      <div class="staging_item staging_item_top">
        <img src="../../../../assets/images/warning_icon.png" alt="" />
        <span>预警中心</span>
      </div>
      <div class="staging_item staging_item_left">
        <img src="../../../../assets/images/analysis_icon.png" alt="" />
        <span>分析中心</span>
      </div>
      <div class="staging_item staging_item_bottom">
        <img src="../../../../assets/images/system_icon.png" alt="" />
        <span>系统中心</span>
      </div>
      <div class="staging_item staging_item_right">
        <img src="../../../../assets/images/subsystem_icon.png" alt="" />
        <span>子系统中心</span>
      </div>
      <div class="tabs">
        <ul>
          <li v-for="item in tabs.tabsList" :key="item.value" @click="changeTab(item)">
            <span :class="{ active: item.value === actived }">
              {{ item.label }}
            </span>
          </li>
        </ul>
      </div>
      <div class="close" @click="doClose">
        <img src="../../../../assets/images/close.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
  import { reactive, ref } from 'vue';

  const props = defineProps(['onClose']);

  const tabs = reactive({
    tabsList: [
      {
        value: 0,
        label: '视频监控',
      },
      {
        value: 1,
        label: '能耗管理',
      },
      {
        value: 2,
        label: '楼宇智控',
      },
      {
        value: 3,
        label: '智能照明',
      },
      {
        value: 4,
        label: '电梯监控',
      },
      {
        value: 6,
        label: '环境检测',
      },
      {
        value: 7,
        label: '资产管理',
      },
      {
        value: 9,
        label: '智能会议',
      },
      {
        value: 10,
        label: '智慧消防',
      },
      {
        value: 11,
        label: '防盗报警',
      },
      {
        value: 12,
        label: '智慧门禁',
      },
      {
        value: 13,
        label: '智慧停车',
      },
      {
        value: 14,
        label: '信息发布',
      },
      {
        value: 15,
        label: '公共广播',
      },
      {
        value: 16,
        label: '电子巡更',
      },
      {
        value: 17,
        label: '工单子系统',
      },
      {
        value: 17,
        label: '群控系统',
      },
    ],
  });
  const actived = ref(0);
  function changeTab(item) {
    actived.value = item.value;
  }

  function doClose() {
    props.onClose()
  }
</script>

<style lang="less" scoped>
  .dialog {
    position: fixed;

    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(10, 22, 48, 0.8);

    .staging {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 500px;
      height: 500px;
      background: ;
      box-shadow: 0px 0px 19px 1px rgba(43, 103, 255, 0.5);
      border-radius: 50%;
      background: url('../../../../assets/images/staging_bg.png') top left no-repeat
        rgba(11, 20, 58, 0.8);
      background-size: 100% auto;

      .staging_item {
        width: 124px;
        height: 126px;
        border-radius: 50%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        span {
          font-size: 20px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #ffffff;
          line-height: 26px;
          margin-top: 12px;
        }
      }

      .staging_item_top {
        position: absolute;
        top: 0;
        left: 50%;
        transform: translateX(-50%);
        margin-top: 40px;
        background: url('../../../../assets/images/warning_bg.png') top left no-repeat;
        background-size: 100% auto;
      }

      .staging_item_left {
        position: absolute;
        top: 50%;
        left: 0;
        transform: translateY(-50%);
        background: url('../../../../assets/images/analysis_bg.png') top left no-repeat;
        background-size: 100% auto;
        margin-left: 40px;
      }

      .staging_item_bottom {
        position: absolute;
        left: 50%;
        bottom: 0;
        transform: translateX(-50%);
        background: url('../../../../assets/images/system_bg.png') top left no-repeat;
        background-size: 100% auto;
        margin-bottom: 40px;
      }

      .staging_item_right {
        position: absolute;
        top: 50%;
        right: 0;
        transform: translateY(-50%);
        background: url('../../../../assets/images/subsystem_bg.png') top left no-repeat;
        background-size: 100% auto;
        margin-right: 40px;
      }

      .tabs {
        position: absolute;
        right: -360px;
        width: 300px;
        height: 460px;
        background: #0b143a;
        box-shadow: 0px 0px 19px 1px rgba(43, 103, 255, 0.5);

        ul {
          width: 100%;
          padding: 20px 20px;
          display: flex;
          justify-content: space-between;
          flex-wrap: wrap;

          li {
            width: 50%;
            text-align: center;
            cursor: pointer;
            span {
              font-size: 16px;
              font-family: Microsoft YaHei;
              font-weight: 400;
              color: #b4c0db;
              line-height: 48px;
              padding: 0 18px;
              &.active {
                display: inline-block;
                background: rgba(141, 36, 0, 0.34);
                border: 1px solid #f6bd56;
                color: #fff;
                box-shadow: 0px 0px 16px 2px #ff630e, 0px 0px 66px 4px rgba(255, 99, 14, 0.18);
              }
            }
          }
        }
      }
      .close {
        position: absolute;
        color: #fff;
        width: 30px;
        height: 30px;
        right: 20px;
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
</style>
