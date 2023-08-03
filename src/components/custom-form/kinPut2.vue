<template>
  <div>
    <!-- 自定义组件要实现v-model  必须实现：value  @input -->
    <!-- <input type="text" :value="modelValue" @input="oninput" />
    {{ modelValue }} -->
    input2
    <input :value="modelValue" type="text" @input="oninput">
    {{ modelValue }}
    <!-- <button @click="oninput">+1</button> -->
  </div>
</template>

<script>
export default {
  // model: {
  //   prop: "activeIndex",
  //   event: "update",
  // },
  // props: {
  //   modelValue: {
  //     type: String,
  //     default: "",
  //   },
  // },
  model: {
    prop: 'modelValue',
    event: "update:modelValue"
  },
  props: {
    modelValue: {
      type: String,
      default: "12"
    }
  },
  data() {
    return {};
  },
  methods: {
    oninput(e) {
      // 通知父组件数据得变化
      this.$emit("update:modelValue", e.target.value);
      console.log(e.target.value, "this.modelValue+1");
    },
  },
};
</script>

<style scoped></style>