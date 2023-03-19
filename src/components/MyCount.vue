<template>
  <div id="MyCount-container">
    <h5>MyCount组件 是 子组件 , 现在是 子 传 父 </h5>
    <h5>MyCount 的 count值为 {{ count }} </h5>
    <button @click="add(1, $event)"> +1 </button>
  </div>
</template>

<script>
export default {
  name: 'MyCount',
  data() {
    return {
      count: 0,
    }
  },
  methods: {
    add(n, e) {
      this.count += n;
      console.log(e);
      this.$emit('numChange', this.count)
    }
  }
}
</script>

<style scoped>
#MyCount-container {
  width: 400px;
  height: 300px;
  margin: auto 100px auto 100px;
  background-color: aquamarine;
}
</style>
