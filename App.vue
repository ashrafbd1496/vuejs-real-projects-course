<template>
  <div class="wrapper flex flex-col justify-center items-center">
    <img
      id="lifecyclehook"
      class="lifecyclehook w-24 h-auto"
      src="./assets/vue.svg"
      alt=""
    />
  </div>

  <script>
    //import Hooks from "./components/Hooks.vue";

    export default {
      name: "App",
      components: {
        //Hooks,
      },
      data() {
        return {};
      },

      mounted() {},
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
</template>
