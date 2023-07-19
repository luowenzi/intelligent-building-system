<template>
    <div class="overview">
        <div class="pageTitle">
            <i></i>
            <span>项目概况</span>
        </div>
        <div class="content">
            <div class="build">
                <span class="count">6738㎡</span>
                <span class="count">建筑面积</span>
            </div>
            <div class="coverArea">
                <span class="count">5989㎡</span>
                <span class="count">占地面积</span>
            </div>
            <div class="building">
                <span class="count">15</span>
                <span class="count">楼栋数量</span>
            </div>
        </div>
    </div>
</template>
<script setup lang="ts">

</script>
<style lang="less" scoped>
.overview {
    width: 400px;
    height: 220px;
    background: rgba(13, 26, 57, 0.8);
    border: 1px solid #1C3762;
    box-shadow: 0px 0px 30px 0px rgba(16, 61, 115, 0.8);
    padding: 8px 0;

    .content {
        position: relative;
        width: 100%;
        height: calc(100% - 40px);

        .build,
        .coverArea,
        .building {
            width: 100px;
            height: 90px;
            border-radius: 50%;
            position: absolute;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            span:first-child {
                font-size: 22px;
                font-family: TsangerJinKai05-6763;
                font-weight: normal;
                color: #FFFFFF;
            }

            span:last-child {
                font-size: 16px;
                font-family: Microsoft YaHei;
                font-weight: 400;
                color: #FFFFFF;
            }
        }
        .build {
            background: #387FE8;
            bottom: 23px;
            left: 25px;
        }

        .coverArea {
            top: 29px;
            right: 143px;
            background: #DA6C75;
        }

        .building {
            right: 25px;
            bottom: 24px;
            background: #5AC64F;
        }
    }
}
</style>