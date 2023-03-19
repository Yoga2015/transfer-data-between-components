<template>
  <div id="Top-container">
    <h4> Top组件 是 父组件 , Top 传 Son 的数据 是 {{ fatherInit }}</h4>
    <Son :init="fatherInit"></Son>
  </div>
</template>
  
<script>
import Son from "@/components/Son.vue";

export default {
  name: 'MyTop',
  data() {
    return {
      fatherInit: 20
    }
  },
  components: {
    Son
  }
}
</script>

<style>
#Top-container {
  background-color: yellow;
  padding: 5px;
  flex: 1,
}
</style>