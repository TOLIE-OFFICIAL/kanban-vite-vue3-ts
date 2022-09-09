<!--  -->
<template>
  <div class="list">
    <h3 class="list-title">{{ list }}</h3>
    <button class="list-btn">+</button>
    <ul class="list-content">
      <li class="list-items" v-for="item in 100" key="item">
        <h3 class="list-items-title"><i>·</i>Hi!</h3>
        <p class="list-items-content">这是第{{ item }}个事项这是第{{ item }}个事项这是第{{
          item
        }}个事项这是第{{ item }}个事项 这是第{{ item }}个事项这是第{{
          item
        }}个事项这是第{{ item }}个事项这是第{{ item }}个事项</p>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
type Props = {
  list?: string;
};
defineProps<Props>();
</script>
<style lang="less">
.list {
  display: flex;
  flex-direction: column;
  flex: 1;
  margin-right: 50px;
  padding: 0 10px;
  border: 1px solid #ccc;
  background-color: #ededed;
  border-radius: 10px;
  &:last-child {
    margin-right: 0;
  }
  &-title {
    height: 38px;
    line-height: 38px;
    font-style: italic;
    font-weight: 700;
    font-size: 20px;
    color: #3399cc;
  }
  &-btn {
    height: 28px;
    font-weight: bold;
    &:hover {
      cursor: pointer;
    }
  }
  &-content {
    flex: 1;
    overflow-y: auto;
    .list-items {
      margin-top: 16px;
      padding: 10px;
      background-color: #fefefe;
      border-radius: 8px;
      &:last-child {
        margin-bottom: 10px;
      }
      &-title {
        font-size: 20px;
        margin-bottom: 3px;
        i {
          background-color: #ff6600;
          display: inline-block;
          margin-right: 8px;
          height: 8px;
          width: 8px;
          border-radius: 50%;
          vertical-align: middle;
        }
      }
      &-content{
        font-size: 14px;
        color: #3c3c3c;
      }
    }
  }
}
</style>
