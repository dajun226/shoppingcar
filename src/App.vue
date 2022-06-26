<template>
  <div class="app">
    <MyHeader title="购物车"></MyHeader>
    <MyGoods></MyGoods>
    <MyFooter></MyFooter>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyGoods from './components/MyGoods.vue'
import MyFooter from './components/MyFooter.vue'
export default {
  // 引入组件
  components: {
    MyHeader,
    MyGoods,
    MyFooter
  }
}
</script>

<style scoped>
/* 让内容下移 */
.app{
  padding: 50px 0;
}
</style>>