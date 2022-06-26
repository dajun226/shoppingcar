<template>
  <div class="app">
    <MyHeader title="购物车"></MyHeader>
    <MyGoods 
    v-for="item in goodsList"
    :key="item.goods_id"
    :goods="item"
    ></MyGoods>
    <MyFooter :goodsList="goodsList"></MyFooter>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyGoods from './components/MyGoods.vue'
import MyFooter from './components/MyFooter.vue'
import axios from 'axios'
export default {
  // 引入组件
  components: {
    MyHeader,
    MyGoods,
    MyFooter
  },
  data() {
    return {
      goodsList:[]
    }
  },
  created() {
    this.getGoods()
  },
  methods: {
    async getGoods(){
      const res = await axios({ url: '/api/cart' })
      this.goodsList = res.data.list
    }
  }
}
</script>

<style scoped>
/* 让内容下移 */
.app{
  padding: 50px 0;
}
</style>>