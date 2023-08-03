<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  provide() {
    return {
      form: this, //传递form实例给后代，比如
    };
  },
  //   data() {
  //     return {
  //       key: value,
  //     };
  //   },
  props: {
    model: {
      type: Object,
      require: true,
    },
    rule: {
      type: Object,
    },
  },
};
</script>

<style scoped></style>