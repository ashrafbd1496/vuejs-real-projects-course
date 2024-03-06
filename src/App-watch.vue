<template>
  <div class="wrapper flex flex-col justify-center items-center">
    <img
      ref="vueLogo"
      id="lifecyclehook"
      class="lifecyclehook w-24 h-auto"
      src="./assets/vue.svg"
      alt=""
    />
    <h1>Ref Watch</h1>
    <p class="text-xs">Open console to watch</p>
    <h2 class="block w-full" ref="counterRef">{{ counter }}</h2>
    <button @click="counter++" type="button" class="bg-teal-500 px-2 mt-1">
      Click to watch
    </button>
  </div>
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
      counter: 0,
    };
  },

  watch: {
    counter(newValue, OldValue) {
      if (newValue > 5) {
        this.$refs.counterRef.style.background = "red";
      }
      if (OldValue > 7) {
        this.$refs.counterRef.style.background = "green";
      }
    },
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
