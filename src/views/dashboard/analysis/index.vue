<template>
  <div class="block_24 flex-col">
    <img
      class="thumbnail_10"
      referrerpolicy="no-referrer"
      src="https://lanhu.oss-cn-beijing.aliyuncs.com/ps36lq55o3w7qo6ak6bxtmchs1sbx80gbs8247bff2-cd49-45e2-8f36-3cc7d933029b"
    />
    <span class="text_83">首页</span>
    <img
      class="thumbnail_11"
      referrerpolicy="no-referrer"
      src="https://lanhu.oss-cn-beijing.aliyuncs.com/psfh2lb77utk65zd7epp0957h3pen4freq7a5264f6c-f4a9-4d5e-b0de-6084c3bd27b3"
    />
    <span class="text_84">楼宇</span>
    <div class="section_12 flex-col">
      <img
        class="thumbnail_12"
        referrerpolicy="no-referrer"
        src="https://lanhu.oss-cn-beijing.aliyuncs.com/ps7nfb7x2lz35gtg65ff893tngr7s8lo02se1afb6f0-8d4f-4743-bc1b-8b5437a3e626"
      />
      <span class="text_85">能耗</span>
    </div>
    <img
      class="thumbnail_13"
      referrerpolicy="no-referrer"
      src="https://lanhu.oss-cn-beijing.aliyuncs.com/psw0lpgoukrzkkrd6ftg4bwxrpljf898ym1a76cce8-696d-4da9-8c31-2608b89865c9"
    />
    <span class="text_86">照明</span>
    <div class="image-text_6 flex-col justify-between">
      <img
        class="thumbnail_14"
        referrerpolicy="no-referrer"
        src="https://lanhu.oss-cn-beijing.aliyuncs.com/psy21knkmr84kv8wg5ju5bhq4mteun8sz2e3519fba6-262e-4626-8a0c-b265d9c2de9b"
      />
      <span class="text-group_6">通行</span>
    </div>
    <div class="image-text_7 flex-col justify-between">
      <img
        class="thumbnail_15"
        referrerpolicy="no-referrer"
        src="https://lanhu.oss-cn-beijing.aliyuncs.com/pssfcguf1psyg5kfqwfzxva5xl8r6reab81acd3b4-87af-42c2-a614-37e8e664b248"
      />
      <span class="text-group_7">安全</span>
    </div>
    <div class="image-text_8 flex-col justify-between">
      <img
        class="thumbnail_16"
        referrerpolicy="no-referrer"
        src="https://lanhu.oss-cn-beijing.aliyuncs.com/pscx3v3z75hih116g5uak4s82o04sj86wto130dda67-ebf6-4c42-9336-e2ca24a9dadd"
      />
      <span class="text-group_8">资产</span>
    </div>
    <div class="image-text_9 flex-col justify-between">
      <img
        class="thumbnail_17"
        referrerpolicy="no-referrer"
        src="https://lanhu.oss-cn-beijing.aliyuncs.com/psk6qk98pn4omnafjl4vheydjrsg4ssiumc76d73ca-39cc-4338-8e9c-aa532acfd214"
      />
      <span class="text-group_9">联动</span>
    </div>
    <div class="group_22 flex-row" @click="showModal">
      <div class="image-text_1 flex-col justify-between">
        <div class="group_23 flex-col">
          <div class="group_24 flex-col"></div>
          <div class="group_25 flex-col"></div>
          <img
            class="label_1"
            referrerpolicy="no-referrer"
            src="https://lanhu.oss-cn-beijing.aliyuncs.com/ps6hzoy8pbbwrt8l3hrets2mkgyuqgjjdnc020b7d46-2dc8-4259-b572-d5fababe31a3"
          />
        </div>
        <span class="text-group_1">功能箱</span>
      </div>
    </div>
  </div>
  <div class="p-4">
    <HeaderVue />
    <div class="content">
      <Grid-left />
      <Grid-right />
      <totalVue />
    </div>
  </div>
  <a-modal
    v-model:visible="open"
    :title="false"
    @ok="handleOk"
    :footer="false"
    width="100%"
    height="100%"
    :closable="false"
  >
    <Dialog :onClose="onClose" />
  </a-modal>
</template>
<script lang="ts" setup>
  import { ref } from 'vue';
  import GridLeft from './components/GridLeft.vue';
  import GridRight from './components/GridRight.vue';
  import HeaderVue from './components/Header.vue';
  import totalVue from './components/total.vue';
  import Dialog from './components/dialog.vue';

  const loading = ref(true);
  const open = ref<boolean>(false);

  const showModal = () => {
    open.value = true;
  };
  const onClose = () => {
    open.value = false;
  };

  const handleOk = (e: MouseEvent) => {
    console.log(e);
    open.value = false;
  };

  setTimeout(() => {
    loading.value = false;
  }, 1500);
</script>
<style lang="less" scoped>
  .p-4 {
    width: 100%;
    height: 100%;
    background: url('/@/assets/images/bg.png') top left;
    background-size: 100% auto;
    .content {
      margin-top: 50px;
      margin-left: 80px;
      // display: flex;
      overflow: hidden;
    }
  }
</style>
<style lang="less">
  .block_24 {
    background-color: rgba(7, 33, 68, 1);
    position: absolute;
    left: 0;
    width: 72px;
    height: 807px;
    .thumbnail_10 {
      width: 16px;
      height: 16px;
      margin: 123px 0 0 28px;
    }
    .text_83 {
      width: 24px;
      height: 13px;
      overflow-wrap: break-word;
      color: rgba(255, 255, 255, 1);
      font-size: 12px;
      font-family: MicrosoftYaHei;
      font-weight: NaN;
      text-align: center;
      white-space: nowrap;
      line-height: 17px;
      margin: 8px 0 0 24px;
    }
    .thumbnail_11 {
      width: 17px;
      height: 16px;
      margin: 28px 0 0 28px;
    }
    .text_84 {
      width: 24px;
      height: 13px;
      overflow-wrap: break-word;
      color: rgba(255, 255, 255, 1);
      font-size: 12px;
      font-family: MicrosoftYaHei;
      font-weight: NaN;
      text-align: center;
      white-space: nowrap;
      line-height: 17px;
      margin: 8px 0 0 24px;
    }
    .section_12 {
      background-color: rgba(20, 74, 127, 1);
      border-radius: 4px;
      width: 56px;
      height: 56px;
      margin: 18px 0 0 8px;
      .thumbnail_12 {
        width: 14px;
        height: 20px;
        margin: 9px 0 0 21px;
      }
      .text_85 {
        width: 24px;
        height: 11px;
        overflow-wrap: break-word;
        color: rgba(255, 255, 255, 1);
        font-size: 12px;
        font-family: MicrosoftYaHei;
        font-weight: NaN;
        text-align: center;
        white-space: nowrap;
        line-height: 17px;
        margin: 6px 0 10px 16px;
      }
    }
    .thumbnail_13 {
      width: 18px;
      height: 18px;
      margin: 19px 0 0 27px;
    }
    .text_86 {
      width: 23px;
      height: 11px;
      overflow-wrap: break-word;
      color: rgba(255, 255, 255, 1);
      font-size: 12px;
      font-family: MicrosoftYaHei;
      font-weight: NaN;
      text-align: center;
      white-space: nowrap;
      line-height: 17px;
      margin: 7px 0 0 24px;
    }
    .image-text_6 {
      width: 24px;
      height: 36px;
      margin: 29px 0 0 24px;
      .thumbnail_14 {
        width: 17px;
        height: 17px;
        margin-left: 4px;
      }
      .text-group_6 {
        width: 24px;
        height: 11px;
        overflow-wrap: break-word;
        color: rgba(255, 255, 255, 1);
        font-size: 12px;
        font-family: MicrosoftYaHei;
        font-weight: NaN;
        text-align: center;
        white-space: nowrap;
        line-height: 17px;
        margin-top: 8px;
      }
    }
    .image-text_7 {
      width: 24px;
      height: 37px;
      margin: 28px 0 0 24px;
      .thumbnail_15 {
        width: 16px;
        height: 20px;
        margin-left: 5px;
      }
      .text-group_7 {
        width: 24px;
        height: 11px;
        overflow-wrap: break-word;
        color: rgba(255, 255, 255, 1);
        font-size: 12px;
        font-family: MicrosoftYaHei;
        font-weight: NaN;
        text-align: center;
        white-space: nowrap;
        line-height: 17px;
        margin-top: 6px;
      }
    }
    .image-text_8 {
      width: 24px;
      height: 36px;
      margin: 29px 0 0 24px;
      .thumbnail_16 {
        width: 17px;
        height: 17px;
        margin-left: 4px;
      }
      .text-group_8 {
        width: 24px;
        height: 11px;
        overflow-wrap: break-word;
        color: rgba(255, 255, 255, 1);
        font-size: 12px;
        font-family: MicrosoftYaHei;
        font-weight: NaN;
        text-align: center;
        white-space: nowrap;
        line-height: 17px;
        margin-top: 8px;
      }
    }
    .image-text_9 {
      width: 24px;
      height: 36px;
      margin: 29px 0 193px 24px;
      .thumbnail_17 {
        width: 17px;
        height: 17px;
        margin-left: 4px;
      }
      .text-group_9 {
        width: 24px;
        height: 11px;
        overflow-wrap: break-word;
        color: rgba(255, 255, 255, 1);
        font-size: 12px;
        font-family: MicrosoftYaHei;
        font-weight: NaN;
        text-align: center;
        white-space: nowrap;
        line-height: 17px;
        margin-top: 8px;
      }
    }
  }
  .group_22 {
    background-color: rgba(7, 33, 68, 1);
    width: 72px;
    height: 90px;
    margin-top: 219px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    .image-text_1 {
      width: 42px;
      height: 66px;
      margin: 12px 0 0 15px;
      .group_23 {
        background-image: linear-gradient(
          30deg,
          rgba(255, 44, 84, 1) 0,
          rgba(255, 44, 84, 1) 0,
          rgba(255, 198, 131, 1) 100%,
          rgba(255, 198, 131, 1) 100%
        );
        border-radius: 50%;
        position: relative;
        width: 40px;
        height: 40px;
        overflow: hidden;
        margin-left: 1px;
        .group_24 {
          background-image: linear-gradient(
            30deg,
            rgba(255, 58, 97, 0.5) 0,
            rgba(255, 58, 97, 0.5) 0,
            rgba(255, 209, 128, 0.5) 100%,
            rgba(255, 209, 128, 0.5) 100%
          );
          border-radius: 50%;
          position: absolute;
          left: 13px;
          top: 13px;
          width: 26px;
          height: 28px;
        }
        .group_25 {
          background-color: rgba(255, 255, 255, 0.2);
          border-radius: 50%;
          position: absolute;
          left: 0;
          top: 0;
          width: 16px;
          height: 20px;
        }
        .label_1 {
          position: absolute;
          left: 8px;
          top: 8px;
          width: 24px;
          height: 24px;
        }
      }
      .text-group_1 {
        width: 42px;
        height: 14px;
        overflow-wrap: break-word;
        color: rgba(255, 255, 255, 1);
        font-size: 14px;
        font-family: MicrosoftYaHei;
        font-weight: NaN;
        text-align: center;
        white-space: nowrap;
        line-height: 17px;
        margin-top: 12px;
      }
    }
  }
  .ant-modal {
    top: 0;
    .ant-modal-content {
      background: none;
    }
    .ant-modal-body {
      padding: 0;
    }
  }
</style>
