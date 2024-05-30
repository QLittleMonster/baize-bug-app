<template>
  <u-sticky :bgColor="tabStyle().stickyBg">
    <u-tabs
        lineHeight="0"
        :itemStyle="tabStyle().itemStyle"
        :list="tabList"
        :activeStyle="tabStyle().active"
        :inactiveStyle="tabStyle().inactive"
        @click="tabClick"
        keyName="name"
        :scrollable="false"
    ></u-tabs>
  </u-sticky>
</template>
<script setup lang="ts">
import {ref} from "vue"
import {tabs as tabStyle} from "@/config/uview/style";

interface INF_TAB_ITEM {
  name: string
}
const tabList = ref<INF_TAB_ITEM[]>([
  {
    name: '待接单'
  },
  {
    name: '进行中'
  },
  {
    name: '已完成'
  }
])

/** method */
const tabClick = function (item:INF_TAB_ITEM) {
  console.log(item.name,'ff')
}
</script>

<style lang="scss" scoped>
.c{
  border-bottom: 1px solid;
}
</style>