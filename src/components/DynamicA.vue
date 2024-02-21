<template>
  <div>
    <h2>Dynamic Component A</h2>
    <h2 @click="count++">
      <button type="button" class="bg-blue-500 text-white px-2">Counter</button>
      : {{ count }}
    </h2>
  </div>
</template>
<script>
export default {
  name: "DynamicA",
  mounted() {
    console.log('DynamicA component has been mounted');
  },

  beforeDestroy() {
    console.log('DynamicA component is about to be destroyed');
  },

  data() {
    return {
      count: 0,
    };
  },
};
</script>
<style scoped></style>
