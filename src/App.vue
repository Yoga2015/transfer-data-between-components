<template>
  <div id="app">
    <h3> 父子关系的组件之间 传递数据 : 现在是 父 传 子</h3>
    <div class="box">
      <Top></Top>
      <Down></Down>
    </div>

    <div>
      <h3>父子关系的组件之间 传递数据 : 现在是 子 传 父</h3>
    </div>

    <div class="box2">
      <Left></Left>
      <Right></Right>
    </div>


    <div>
      <h3>兄弟、姐妹关系的组件之间 传递数据 </h3>
    </div>

    <div class="box3">
      <Brother></Brother>
      <Sister></Sister>
    </div>
  </div>
</template>

<script>
import Top from '@/components/Top.vue'
import Down from '@/components/Down.vue'
import Left from '@/components/Left.vue'
import Right from '@/components/Right.vue'
import Brother from '@/components/MyBrother.vue'
import Sister from '@/components/MySister.vue'

export default {
  name: 'App',
  components: {
    Top, Down, Left, Right, Brother, Sister
  },
}
</script>

<style>
#app {
  width: auto;
  padding: 1px 20px 20px;
  background-color: antiquewhite;
}

.box {
  display: flex;
}

.box2 {
  display: flex;
}

.box3 {
  display: flex;
}
</style>
