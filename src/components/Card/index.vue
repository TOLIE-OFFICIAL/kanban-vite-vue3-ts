<!-- 全局组件小卡片 -->
<template>
  <div class="card">
    <div class="card-header">
      <div>主标题</div>
      <div>副标题</div>
    </div>
    <div class="card-content" v-if="content">
      {{ content }}
    </div>
  </div>
</template>

<script setup lang="ts">
// 通过Props从父组件向子组件传递数据
type Props = {
  content?: string;
};
defineProps<Props>();
</script>
<style lang="less" scoped>
@border: #ccc;
.card {
  border: 1px solid @border;
  &:hover{
    box-shadow: 0 0 10px @border;
  }
  &-header {
    display: flex;
    padding: 10px;
    justify-content: space-between;
    border-bottom: 1px solid #ccc;
  }
  &-content {
    padding: 10px;
  }
}
</style>
