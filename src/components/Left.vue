<template>
  <div id="Left-container">
    <h3> Left组件 是父组件 </h3>
    <h5> 父 接收 子 传递过来的数据 -- {{ fatherCount }}</h5>
    <MyCount @numChange="getNewCout"></MyCount>
  </div>
</template>

<script>
import MyCount from "@/components/MyCount.vue"

export default {
  name: 'MyLeft',
  data() {
    return {
      fatherCount: 0
    }
  },
  components: {
    MyCount
  },
  methods: {
    getNewCout(val) {
      this.fatherCount = val;
    }
  }
}
</script>

<style>
#Left-container {
  background-color: yellowgreen;
  padding: 5px;
  flex: 1,
}
</style>
