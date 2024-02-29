<template>
  <div class="wrapper flex flex-col justify-center items-center">
    <img ref="vueLogo"
      id="lifecyclehook"
      class="lifecyclehook w-24 h-auto"
      src="./assets/vue.svg"
      alt=""
    />
    <button @click="$refs.vueLogo.style.width='300px'" type="button" class="bg-teal-500 px-2 mt-1">Big</button>
    <button @click="$refs.vueLogo.style.width='100px'" type="button" class="bg-teal-500 mt-1 px-2">Small</button>
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
      
    };
  },

  mounted() {
    
 
  
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
