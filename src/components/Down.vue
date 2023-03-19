<template>
  <div id="Down-container">
    <h4> Down组件 是 父组件 , Down 传 Son 的数据 是 {{ fatherInit }}</h4>
    <Son :init="fatherInit"></Son>
  </div>
</template>

<script>
import Son from "@/components/Son.vue"

export default {
  name: 'MyDown',
  data() {
    return {
      fatherInit: 30
    }
  },
  components: {
    Son
  }
}
</script>

<style>
#Down-container {
  background-color: rgb(56, 230, 230);
  padding: 5px;
  flex: 1,
}
</style>
