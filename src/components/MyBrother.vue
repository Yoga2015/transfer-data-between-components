<template>
  <div id="Brother-container">
    <h3>Brother组件 发送/接收数据 </h3>
    <button @click="send">点击发送古诗给 Sister 组件</button>
    <h5>{{ str }}</h5>
  </div>
</template>

<script>
import eventBus from '@/js/eventBus.js'
export default {
  name: 'MyBrother',
  data() {
    return {
      str: '床前明月光，疑似地上霜'
    }
  },
  methods: {
    // 通过 eventBus 来 发送数据
    send() {
      eventBus.$emit('share', this.str)
    }
  }
}
</script>

<style scoped>
#Brother-container {
  width: 600px;
  height: 400px;
  background-color: skyblue;
  padding: 5px;
  flex: 1,
}
</style>