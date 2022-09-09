<!-- 菜单栏组件 -->
<template>
  <div class="menu">
    左侧菜单栏
  </div>

</template>

<script setup lang="ts">
import { reactive,ref,watch,onMounted,onBeforeMount} from 'vue'
</script>
<style lang='less' scoped>
.menu{
    width: 200px;
    border-right: 1px solid #ccc;
}
</style>