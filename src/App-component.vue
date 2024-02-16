<template>
  <!-- <div class="wrapper w-screen items-center justify-center flex flex-col">
    <heading />
    <div class="bottomWrapper flex justify-between">
      <Content />
      <Side />
    </div>
  </div> -->

  <div class="container mx-auto flex flex-col">

      <!-- Header -->
      <Heading />

      <!-- Main Content -->
      <div class="flex">
        <!-- Main Content Area -->
        <Content />

        <!-- Sidebar (hidden on smaller screens) -->
        <Side />
  
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white p-4 mt-20">
      &copy; 2024 All Rights Reserved
    </footer>
  </div>
</template>

<script>
import Heading from "./components/Heading.vue";
import Content from "./components/Content.vue";
import Side from "./components/Side.vue";
export default {
  components: {
    Heading,
    Content,
    Side,
  },
  data() {
    return {};
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
