<template>
  <div>
    <!-- <Form /> -->
    <DynamicInput />
  </div>
</template>

<script>
//import Form from "./components/Form.vue";
import DynamicInput from "./components/DynamicInput.vue";

export default {
  name: "App",
  components: {
    // Form,
    DynamicInput,
  },
};
</script>
<style>
html,
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
