<!-- 内容组件 -->
<template>
  <div class="content">
    <div class="content-items">
      <List :list="'To do'"></List>
      <List :list="'In procress'"></List>
      <List :list="'Completed'"></List>
    </div>
  </div>
</template>

<script setup lang="ts">
import List from '../../components/List/index.vue';
// import { reactive,ref,watch,onMounted,onBeforeMount} from 'vue'
</script>
<style lang="less" scoped>
.content {
  display: flex;
  flex: 1;
  margin: 20px;
  border: 1px solid #ccc;
  overflow: auto;
  &-items {
    display: flex;
    width: 100%;
    border-bottom: 1px solid #ccc;
    padding: 20px;
  }
}
</style>
