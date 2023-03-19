<template>
  <div id="Son-container">
    <h5>Son组件 是 子组件 , 子 接收 父 传递过来的数据 </h5>
    <h6>Son 的 init值 为 {{ init }} </h6>
  </div>
</template>

<script>
export default {
  name: 'MySon',
  data() {
    return {
      count: 0,
    }
  },

  //props 指向一个数组,
  //允许 使用者 通过 自定义属性, 为 当前的组件 指定初始值
  //自定义属性的名字,是 封装者 自定义的 (只要合法即可)
  // props:[init],

  // props 指向 一个对象
  props: {
    init: {
      type: Number,
      default: 0,
      required: true,
    }
  },
}
</script>

<style scoped>
#Son-container {
  width: 400px;
  height: 300px;
  margin: auto 100px auto 100px;
  background-color: aquamarine;
}
</style>
