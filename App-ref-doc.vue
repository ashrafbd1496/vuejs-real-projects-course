<template>
  <div class="wrapper flex flex-col justify-center items-center">
    <img
      id="lifecyclehook"
      class="lifecyclehook w-24 h-auto"
      src="./assets/vue.svg"
      alt=""
    />
  </div>
  <ul>
    <li v-for="item in list" ref="items">
      {{ item }}
    </li>
  </ul>
  <!-- <input ref="input" type="text" /> -->
</template>

<script>
//import Hooks from "./components/Hooks.vue";

export default {
  name: "App",
  components: {
    //Hooks,
  },
  data() {
    return {
      list: [1, 2, 3, 4],
    };
  },

  mounted() {
    // this.$refs.input.focus();
 
    console.log(this.$refs.items);
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
