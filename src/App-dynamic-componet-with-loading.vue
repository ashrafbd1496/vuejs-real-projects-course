<template>
  <div>
    <!-- <Form /> -->
    <ComponentA v-if="activeComponent ===1" />
    <ComponentB v-if="activeComponent ===0"/>
     <button class="btn btn-sm border-teal-500 m-4 p-1 text-xs" @click="activeComponent=activeComponent=== 1 ? 0 : 1">Change Component</button>
  </div>
</template>

<script>

import {defineAsyncComponent} from "vue";
import loadingComponent from './components/Loading.vue';

import ComponentA from "./components/ComponentA.vue";

const ComponentB = defineAsyncComponent({
  loader: () => {
    return new Promise(resolve => {
      setTimeout(() => {
        resolve(import('./components/ComponentB.vue'));
      }, 5000); // Delay for 5 second (5000 milliseconds)
    });
  },
  loadingComponent: loadingComponent,
});


export default {
  name: "App",
  data(){
    return{
      activeComponent:1,
    };
    
  },
  components: {
    // Form,
    ComponentA,
    ComponentB
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
