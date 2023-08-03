<template>
  <div class="custom-style">
    <label v-if="label">{{ label }}</label>
    <slot></slot>
    <p v-if="jiaoyanmessage">{{ jiaoyanmessage }}</p>
  </div>
</template>

<script>

export default {
  // 挂在得时候进行校验
  //  1. 分不清  谁  也就是哪个组件做什么？？？/
  mounted() {
    console.log(this)
    // this.$on("validate", () => {
    //   this.validate();
    // });
  },
  //   通过注入
  inject: ["form"],
  methods: {
    validate() {
      // 执行组件校验
      // 1.获取校验规则
      // 2.获取数值
    },
  },
  props: {
    label: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      jiaoyanmessage: "",
    };
  },
};
</script>

<style scoped>
.custom-style {
  background-color: aqua;
  margin-bottom: 10px;
}
</style>