<template>
  <div class="grid_right">
    <work-status></work-status>
    <MeetingRoomVue></MeetingRoomVue>
    <AlarmVue></AlarmVue>
  </div>
</template>
<script setup lang="ts">
import AlarmVue from './Alarm.vue'
import MeetingRoomVue from './MeetingRoom.vue'
import workStatus from './WorkStatus.vue'
</script>
<style lang="less" scoped>
.grid_right {
  float: right;
}
</style>