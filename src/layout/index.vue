<!--  -->
<template>
  <div class="layout">
    <Menu></Menu>
    <div class="layout-right">
      <Header></Header>
      <Content></Content>
    </div>
  </div>
</template>

<script setup lang="ts">
// 这些就是局部组件，必须在需要的地方引入后使用
import Header from "./Header/index.vue";
import Menu from "./Menu/index.vue";
import Content from "./Content/index.vue";
</script>
<style lang="less" scoped>
.layout {
  display: flex;
  height: 100%;
  overflow: hidden;
  &-right {
    display: flex;
    flex: 1;
    flex-direction: column;
  }
}
</style>
