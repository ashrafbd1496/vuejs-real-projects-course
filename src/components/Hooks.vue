<template>
  <div>
    <h2 class="text-2xl font-extrabold">Vue Lifecycle Hooks</h2>
  
    <!-- <p>{{ counter }}</p>
    <button
      @click="increment"
      type="button"
      class="bg-cyan-700 text-white border-solid px-2 py-1"
    >
      Increment
    </button> -->
  </div>
</template>
<script>
export default {
  name: "Hooks",
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    increment() {
      this.counter++;
    },
  },
  beforeMount(){
    console.log('Before Mount');
  },
  unmounted() {
    console.log('unmounted');
  },
  // beforeUpdate() {
  //   console.log(
  //     `Counter value is about to  changed from ${this.counter} to ${
  //       this.counter + 1
  //     } `
  //   );
  // },
  // updated() {
  //   console.log(
  //     `Counter value has changed from ${this.counter - 1} to ${this.counter}`
  //   );
  // },
};
</script>
<style scoped>
</style>
