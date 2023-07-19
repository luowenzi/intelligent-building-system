<template>
  <div class="alarm">
    <div class="pageTitle">
      <i></i>
      <span>告警事件</span>
    </div>
    <a-table size="small" :data-source="dataSource" :columns="columns" :pagination="false">
      <template #bodyCell="{ column, text, record }">
        <template v-if="column.dataIndex === 'name'">
          <div class="editable-cell">
            <div v-if="editableData[record.key]" class="editable-cell-input-wrapper">
              <a-input
                v-model:value="editableData[record.key].name"
                @pressEnter="save(record.key)"
              />
              <check-outlined class="editable-cell-icon-check" @click="save(record.key)" />
            </div>
            <div v-else class="editable-cell-text-wrapper">
              {{ text || ' ' }}
              <edit-outlined class="editable-cell-icon" @click="edit(record.key)" />
            </div>
          </div>
        </template>
      </template>
    </a-table>
  </div>
</template>
<script lang="ts" setup>
  import { computed, reactive, ref } from 'vue';
  import type { Ref, UnwrapRef } from 'vue';
  import { CheckOutlined, EditOutlined } from '@ant-design/icons-vue';
  import { cloneDeep } from 'lodash-es';

  interface DataItem {
    key: string;
    type: string;
    msg: string;
    state: string;
    time: string;
  }

  const columns = [
    {
      title: '告警时间',
      dataIndex: 'time',
      width: '30%',
    },
    {
      title: '告警类型',
      dataIndex: 'type',
    },
    {
      title: '告警信息',
      dataIndex: 'msg',
    },
    {
      title: '处理状态',
      dataIndex: 'state',
    },
    {
      title: '操作',
      dataIndex: 'operation'
    },
  ];
  const dataSource: Ref<DataItem[]> = ref([
    {
      key: '0',
      time: '1分钟前',
      type: '安防',
      msg: '越界行为',
      state: '处理中',
    },
    {
      key: '1',
      time: '1分钟前',
      type: '安防',
      msg: '越界行为',
      state: '处理中',
    },
  ]);
  const count = computed(() => dataSource.value.length + 1);
  const editableData: UnwrapRef<Record<string, DataItem>> = reactive({});

  const edit = (key: string) => {
    editableData[key] = cloneDeep(dataSource.value.filter((item) => key === item.key)[0]);
  };
  const save = (key: string) => {
    Object.assign(dataSource.value.filter((item) => key === item.key)[0], editableData[key]);
    delete editableData[key];
  };

  const onDelete = (key: string) => {
    console.log(key);
  };
</script>
<style lang="less" scoped>
  .editable-cell {
    position: relative;
    .editable-cell-input-wrapper,
    .editable-cell-text-wrapper {
      padding-right: 24px;
    }

    .editable-cell-text-wrapper {
      padding: 5px 24px 5px 5px;
    }

    .editable-cell-icon,
    .editable-cell-icon-check {
      position: absolute;
      right: 0;
      width: 20px;
      cursor: pointer;
    }

    .editable-cell-icon {
      margin-top: 4px;
      display: none;
    }

    .editable-cell-icon-check {
      line-height: 28px;
    }

    .editable-cell-icon:hover,
    .editable-cell-icon-check:hover {
      color: #108ee9;
    }

    .editable-add-btn {
      margin-bottom: 8px;
    }
  }
  .editable-cell:hover .editable-cell-icon {
    display: inline-block;
  }
  .ant-table {
    background: none;
  }
</style>
<style lang="less" scoped>
  .alarm {
    width: 400px;
    height: 309px;
    margin-top: 5px;
    background: rgba(13, 26, 57, 0.8);
    border: 1px solid #1c3762;
    box-shadow: 0px 0px 30px 0px rgba(16, 61, 115, 0.8);
  }
</style>
