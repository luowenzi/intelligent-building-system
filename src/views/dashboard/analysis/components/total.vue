<template>
  <div class="total">
    <ul>
      <li>
        <div class="con">
          <div class="count">
            <span>180</span>
            <span>天</span>
          </div>
          <div class="label">
            安全运营
          </div>
        </div>
      </li>
      <li>
        <div class="con">
          <div class="count">
            <span>5270</span>
            <span>件</span>
          </div>
          <div class="label">
            排查隐患
          </div>
        </div>
      </li>
      <li>
        <div class="con">
          <div class="count">
            <span>180</span>
            <span>天</span>
          </div>
          <div class="label">
            安全运营
          </div>
        </div>
      </li>
      <li>
        <div class="con">
          <div class="count">
            <span>180</span>
            <span>天</span>
          </div>
          <div class="label">
            安全运营
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>
<script setup lang="ts">

</script>
<style lang="less" scoped>
.total {
  margin: 0 400px;

  ul {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 96px;

    li {
      width: 150px;
      height: 150px;
      border: 3px dashed #00CFFF;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;

      .con {
        width: 126px;
        height: 126px;
        border: 3px solid #9FD3FF;
        border-radius: 50%;
        background: rgba(23, 74, 116, .3);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
      }

      .count {
        span {
          color: #9FD3FF;
        }

        span:first-child {
          font-size: 28px;
          font-family: 300-CAI978;
          line-height: 19px;
        }

        span:last-child {
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          line-height: 30px;

        }
      }

      .label {
        font-size: 16px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #9FD3FF;
        line-height: 12px;
        margin-top: 16px;
      }

      &:nth-of-type(2) {
        border-color: #FFF09F;

        .con {
          border-color: #FFF09F;
        }

        .count {
          span {
            color: #FFF09F;
          }
        }

        .label {
          color: #FFF09F;
        }
      }

      &:nth-of-type(3) {
        border-color: #50EA21;

        .con {
          border-color: #50EA21;
        }

        .count {
          span {
            color: #50EA21;
          }
        }

        .label {
          color: #50EA21;
        }
      }

      &:nth-of-type(4) {
        border-color: #F7601D;

        .con {
          border-color: #F7601D;
        }

        .count {
          span {
            color: #F7601D;
          }
        }

        .label {
          color: #F7601D;
        }
      }
    }
  }
}
</style>