<template>
  <div class="wrapper flex flex-col justify-center items-center">
    <img
      id="lifecyclehook"
      class="lifecyclehook w-24 h-auto"
      src="./assets/vue.svg"
      alt=""
    />
    <Hooks v-if="show" />
    <button
      @click="show = !show"
      type="button"
      class="bg-teal-500 text-white px-2 mt-2"
    >
      Show/Hide
    </button>
  </div>
</template>

<script>
import Hooks from "./components/Hooks.vue";

export default {
  name: "App",
  components: {
    Hooks,
  },
  data() {
    return {
      show: true,
      // createdHook: "Lifecycle created hook",
      // mountedHook: "Lifecycle mounted hook",
    };
  },
  
  // beforeCreate() {
  //   console.log(this.createdHook);
  // },
  // created() {
  //   console.log(this.createdHook);
  // },
  // beforeMount() {
  //   console.log(this.mountedHook);
  // },
  // mounted() {
  //   console.log(this.mountedHook);
  // },
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
