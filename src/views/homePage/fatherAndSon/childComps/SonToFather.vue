<template>
  <div class="son-to-father">
    <input v-model="value" type="text"/>
    <button @click="sendToFather">点击我发送数据给父组件</button>
  </div>
</template>

<script>

export default {
  name: '',
  components: {},
  props: {},
  data () {
    return {
      value:"组件的数据"
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
    sendToFather() {
      this.$emit("getSonData",this.value);
    }
  }
}
</script>

<style scoped>

/* @import url(); 引入公共css类 */

</style>
