<template>
  <div class="contentWrapper w-screen p-4 bg-gray-300 pt-4 flex grow flex-col">
    <h3 class="text-3xl">Content</h3>
    <Card />
    <Card />
    <Card />
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "Content",
  components: { Card },
};
</script>

<style scoped></style>
