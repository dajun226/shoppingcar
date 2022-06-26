<template>
  <div class="my-header" :style="{background,color}">{{title}}</div>
</template>

<script>
export default {
  props: {
    // 外部插入此变量的值, 必须是字符串类型, 否则报错
    background:String,
    color: {
      // 约束color值的类型
      type: String,
      default:'#fff'
    },
    title: {
      type: String,
      // 必须传入此变量的值
      required:true,
    }
  }
}
</script>

<style lang="less" scoped>
  .my-header {
    height: 45px;
    line-height: 45px;
    text-align: center;
    background-color: #1d7bff;
    color: #fff;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 2;
  }
</style>