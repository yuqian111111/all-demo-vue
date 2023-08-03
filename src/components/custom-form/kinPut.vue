<template>
  <div>
    <!-- 自定义组件要实现v-model  必须实现：value  @input -->
    <!--  attrs  存储得是props之外得东西-->
    input1
    <input :value="title" @input="oninput" v-bind="$attrs" />
    {{ title }}
  </div>
</template>

<script>
export default {
  // 避免顶层得继承
  inheritAttrs: false,
  props: {
    title: {
      type: String,
      default: "",
    },
    label: {
      type: String,
      default: "",
    }
  },

  data() {
    return {};
  },
  methods: {
    oninput(e) {
      // 通知父组件数据得变化
      this.$emit("update:title", e.target.value);
      console.log(e.target.value);
      console.log(this.$parent)
      // 通知进行校验
      this.$parent.$emit("validate");
    },
  },
};
</script>

<style scoped></style>