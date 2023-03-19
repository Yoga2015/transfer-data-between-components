<template>
  <div id="Top-container">
    <h3> Right组件 是父组件 </h3>
    <h5> 父 接收 子 传递过来的数据 -- {{ fatherCount }}</h5>
    <MyCount @numChange="getNewCount"></MyCount>
  </div>
</template>
  
<script>
import MyCount from "@/components/MyCount.vue";

export default {
  name: 'MyRight',
  data() {
    return {
      fatherCount: 0
    }
  },
  components: {
    MyCount
  },
  methods: {
    getNewCount(val) {
      this.fatherCount = val;
    }
  }
}
</script>

<style scoped>
#Top-container {
  background-color: pink;
  padding: 5px;
  flex: 1,
}
</style>
