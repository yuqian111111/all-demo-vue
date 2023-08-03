<template>
  <div>
    <Kform :model="model" :rule="rule">
      <Kformitem label="用户名">
        <KInPut v-model:title="model.username"></KInPut>
        <KInPut2 v-model="model.username"></KInPut2>
      </Kformitem>
      <Kformitem label="密码">
        <!-- <KInPut v-model:test="model.password" type="password"></KInPut> -->
        <!-- <KInPut2 v-model="model.password" type="password"></KInPut2> -->
      </Kformitem>
    </Kform>
    {{ model }}
  </div>
</template>
<script>
// import { getCurrentInstance, ref } from 'vue'
import KInPut2 from "./kinPut2.vue";
import KInPut from "./kinPut.vue";
import Kformitem from "./Kformitem.vue";
import Kform from "./Kform.vue";
// getCurrentInstance()

// console.log(getCurrentInstance())
export default {
  components: {
    KInPut,
    Kformitem,
    Kform,
    KInPut2
  },
  mounted() {
    console.log(this)
  },
  data() {
    return {
      test: "",
      model: {
        username: "",
        password: "",
        age: 18
      },
      rules: {
        username: [{ required: true, message: "用户名必须要填写" }],
        password: [{ required: true, message: "密码必须要填写" }],
      },
    };
  },
  methods: {
    name() { },
  },
};
</script>

<style scoped></style>