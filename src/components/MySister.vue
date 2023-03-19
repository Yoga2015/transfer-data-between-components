<template>
  <div id="Sister-container">
    <h3>Sister组件 发送/接收数据</h3>
    <p>{{ msgFromBrother }}</p>
  </div>
</template>

<script>
import eventBus from '@/js/eventBus.js';
export default {
  name: 'MySister',
  data() {
    return {
      msgFromBrother: ''
    }
  },
  created() {
    // 为 eventBus 绑定 自定义事件share , 监听 share
    eventBus.$on('share', (val) => {
      this.msgFromBrother = val
    })
  }
}
</script>

<style scoped>
#Sister-container {
  width: 600px;
  height: 400px;
  background-color: peru;
  padding: 5px;
  flex: 1,
}
</style>