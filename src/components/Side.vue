<template>
  <div
    class="hidden md:block sideWrapper p-4 w-1/3 bg-gray-300 flex-col justify-center"
  >
    <h3 class="text-3xl">Sidebar</h3>
    <Card height="h-100px" customContent="Our content" />
    <Card height="h-100px" customContent="Our content" />
    <Card height="h-100px" customContent="Our content" />
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "Side",
  components: { Card },
};
</script>

<style scoped></style>
