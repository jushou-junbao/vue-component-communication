<template>
  <div class="father-b">
    <div>
      <h3>兄弟组件1</h3>
      <Brother-one @getSonData="getSonData"></Brother-one>
    </div>
    <br/>
    <div>
      <h3>兄弟组件2</h3>
      <Brother-two ref="borther_b" :brotherData="sonAData"></Brother-two>
    </div>
  </div>
</template>

<script>
import BrotherOne from "./childComps/BrotherOne"
import BrotherTwo from "./childComps/BrotherTwo"
export default {
  name: '',
  components: {
    BrotherOne,
    BrotherTwo
  },
  props: {},
  data () {
    return {
      sonAData: ""
    }
  },
  computed: {},
  watch: {},
  // 生命周期 - 创建完成（可以访问当前this实例,data,props）
  created () {

  },
  // 生命周期 - 挂载完成（可以访问DOM元素）
  mounted () {

  },
  beforeCreate () { }, // 生命周期 - 创建之前
  beforeMount () { }, // 生命周期 - 挂载之前
  beforeUpdate () { }, // 生命周期 - 更新之前
  updated () { }, // 生命周期 - 更新之后
  beforeDestroy () { }, // 生命周期 - 销毁之前
  destroyed () { }, // 生命周期 - 销毁完成
  activated () { }, // 如果页面有keep-alive缓存功能，这个函数会触发
  // 方法集合
  methods: {
    getSonData(value) {
      this.sonAData = value;
    }
  }
}
</script>

<style scoped>

/* @import url(); 引入公共css类 */
.father-b {
  margin-bottom: 100px;
  border: 1px red solid;
}
</style>
