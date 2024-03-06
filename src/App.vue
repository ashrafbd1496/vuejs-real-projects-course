<template>
  <div>
    <Todo />
  </div>
</template>

<script>
import Todo from "./components/Todo.vue";

export default {
  name: "App",
  components: {
    Todo,
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
