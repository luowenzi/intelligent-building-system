<template>
  <div class="electricConsumption">
    <div class="pageTitle">
      <i></i>
      <span>电能耗</span>
    </div>
    <div class="content">
      <div class="pageItem">
        <div class="item">
          <div class="day">
            <span class="label">今日</span>
            <span class="count">15KW/h</span>
          </div>
          <div class="his">
            <span>往年日</span>
            <span class="down">
              -13
              <CaretDownOutlined class="down_icon" />
            </span>
          </div>
        </div>
        <div class="item">
          <div class="day">
            <span class="label">今日</span>
            <span class="count">15KW/h</span>
          </div>
          <div class="his">
            <span>往年日</span>
            <span class="up">
              +13
              <CaretUpOutlined class="up_icon" />
            </span>
          </div>
        </div>
      </div>
      <div class="pageItem">
        <div class="item">
          <div class="day">
            <span class="label">今日</span>
            <span class="count">15KW/h</span>
          </div>
          <div class="his">
            <span>往年日</span>
            <span class="up">
              +13
              <CaretUpOutlined class="up_icon" />
            </span>
          </div>
        </div>
        <div class="item">
          <div class="day">
            <span class="label">今日</span>
            <span class="count">15KW/h</span>
          </div>
          <div class="his">
            <span>往年日</span>
            <span class="down">
              -13
              <CaretDownOutlined class="down_icon" />
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
  import { CaretDownOutlined, CaretUpOutlined } from '@ant-design/icons-vue';
</script>
<style lang="less" scoped>
  .electricConsumption {
    margin-top: 5px;
    width: 400px;
    height: 309px;
    background: rgba(13, 26, 57, 0.8);
    border: 1px solid #1c3762;
    box-shadow: 0px 0px 30px 0px rgba(16, 61, 115, 0.8);

    .content {
      .pageItem {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 20px;
        margin-top: 20px;

        .item {
          width: 170px;
          height: 110px;
          background: rgba(255, 255, 255, 0.04);
          border: 1px solid #2f5187;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;

          .day {
            display: flex;
            align-items: center;

            span:first-child {
              font-size: 16px;
              font-family: Microsoft YaHei;
              font-weight: 400;
              color: #ffffff;
              line-height: 42px;
            }

            span:last-child {
              font-size: 24px;
              font-family: Microsoft YaHei;
              font-weight: 400;
              color: #b4e6ff;
              line-height: 42px;
              margin-left: 10px;
            }
          }

          .his {
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            line-height: 42px;

            span {
              margin-left: 10px;

              .up_icon,
              .down_icon {
                width: 20px;
                display: inline-block;
                height: 20px;
                color: #ff1100;
              }

              .down_icon {
                color: #13da0c;
              }
            }
          }
        }
      }
    }
  }
</style>
