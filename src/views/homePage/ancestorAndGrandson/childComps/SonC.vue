<template>
  <div>
    <div>
      <h3>sonC组件内</h3>
      来自祖先的数：{{ancestorData3}}
      <br/>
      SonC中的$attrs为：{{$attrs}}
    </div>
    <grand-son v-bind="$attrs" v-on="$listeners"></grand-son>
    
  </div>
</template>

<script>
import GrandSon from "./GrandSon";
export default {
  name: "",
  components: {
    GrandSon
  },
  props: {
    ancestorData3: {
      type: String,
      default: ""
    }
  },
  data() {
    return {};
  },
  computed: {},
  watch: {},
  // 生命周期 - 创建完成（可以访问当前this实例,data,props）
  created() {},
  // 生命周期 - 挂载完成（可以访问DOM元素）
  mounted() {},
  beforeCreate() {}, // 生命周期 - 创建之前
  beforeMount() {}, // 生命周期 - 挂载之前
  beforeUpdate() {}, // 生命周期 - 更新之前
  updated() {}, // 生命周期 - 更新之后
  beforeDestroy() {}, // 生命周期 - 销毁之前
  destroyed() {}, // 生命周期 - 销毁完成
  activated() {}, // 如果页面有keep-alive缓存功能，这个函数会触发
  // 方法集合
  methods: {}
};
</script>

<style scoped>
/* @import url(); 引入公共css类 */
</style>
