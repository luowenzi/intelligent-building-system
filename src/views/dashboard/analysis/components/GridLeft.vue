<template>
  <div class="grid-left">
    <Project-overview-vue />
    <Equipment-monitor-vue />
    <Electric-consumption-vue />
  </div>
</template>
<script lang="ts" setup>
  import { ref } from 'vue';
  import ElectricConsumptionVue from './ElectricConsumption.vue';
  import EquipmentMonitorVue from './EquipmentMonitor.vue';
  import ProjectOverviewVue from './ProjectOverview.vue';
  const loading = ref(true);

  setTimeout(() => {
    loading.value = false;
  }, 1500);
</script>
<style lang="less" scoped>
  .grid-left {
    float: left;
  }
</style>
