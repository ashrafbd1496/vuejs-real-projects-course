<template>
  <div
    class="bg-white rounded-xl shadow-md hover:shadow-2xl m-2 p-4"
    :style="{ height: height ? height : '' }"
  >
    <h3>Asrhaf Uddin</h3>
    
    <p>{{ customContent }}</p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["height", "customContent"],
};
</script>

<style scoped></style>
