<template>
  <div>
    <!-- <slotChild></slotChild> -->
    <!-- <practise></practise> -->
    <customForm></customForm>
    <!-- <Customform2></Customform2> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import slotChild from '@/components/soltscope/index.vue';
// import practise from "../components/practise3/index.vue"
import customForm from '@/components/custom-form/index.vue';

export default {
  name: "HomeView",
  components: {
    // slotChild,
    // practise,
    customForm,
  }
};
</script>


<style></style>
