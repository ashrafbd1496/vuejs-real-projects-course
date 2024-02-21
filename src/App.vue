<template>
  <div class="flex justify-center">
    <button
      @click="activeComponent = 'DynamicA'"
      class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded mr-2"
    >
      Component A
    </button>
    <button
      @click="activeComponent = 'DynamicB'"
      class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded mr-2"
    >
      Component B
    </button>
    <button
      @click="activeComponent = 'DynamicC'"
      class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded"
    >
      Component C
    </button>
  </div>

  <div class="mt-4 inline-flex">
    <h2 class="text-xl flex justify-center">
      Active Component content of {{ activeComponent }} :
    </h2>
  </div>
  <keep-alive>
    <component :is="activeComponent" />
  </keep-alive>
</template>

<script>
import DynamicA from "./components/DynamicA.vue";
import DynamicB from "./components/DynamicB.vue";
import DynamicC from "./components/DynamicC.vue";

export default {
  name: "App",
  components: {
    DynamicA,
    DynamicB,
    DynamicC,
  },
  data() {
    return {
      activeComponent: "DynamicA",
    };
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
