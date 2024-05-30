<template>
  <u-cell-group
      :customStyle="{
          'font-size': '32rpx',
          'font-family': 'SourceHanSansCN-Regular-, SourceHanSansCN-Regular',
          'background-color': '#fff'
        }"
      :border="false"
  >
    <u-cell
        v-for="item in cellList"
        :key="item.title"
        clickable
        :title="item.title"
        isLink
        :url="item.url"
        :rightIconStyle="cellStyle()"
    ></u-cell>
  </u-cell-group>
</template>
<script setup lang="ts">
import {ref} from 'vue'
import {cell as cellStyle} from "@/config/uview/style";

const cellList = ref([
  { title: '我的任务', url: '/pages/bug/user/task' },
  { title: '我的需求', url: '/pages/bug/user/demand' },
  { title: '意见反馈', url: '/pages/bug/user/suggest' },
  { title: '规则说明', url: '/pages/bug/user/rules' },
])
</script>
