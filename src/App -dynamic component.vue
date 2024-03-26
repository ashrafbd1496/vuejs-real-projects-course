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
import ComponentA from "./components/ComponentA.vue";


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
    ComponentB:defineAsyncComponent(()=>
    import("./components/ComponentB.vue")),
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
