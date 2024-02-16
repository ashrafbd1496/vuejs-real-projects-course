<template>
  <div class="flex flex-col h-screen mx-auto">
    <!-- Header -->
    <header class="bg-gray-800 text-white p-4 w-screen">Header Content</header>

    <!-- Main Content -->
    <div class="flex flex-grow">
      <!-- Sidebar (hidden on smaller screens) -->
      <aside class="hidden md:block bg-gray-200 w-1/4 p-4">
        Sidebar Content
      </aside>

      <!-- Main Content Area -->
      <main class="flex-grow p-4">
        <Hello>
          <h2 class="text-4xl font-extrabold mb-4">What is slot ?</h2>
          <p class="p-2">
            In Vue.js, a slot is a placeholder in a component's template that
            allows the parent component to inject content into it. Slots are
            useful when you want to create reusable components that can have
            dynamic content.
          </p>
          <button
            type="button"
            class="text-white bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800 shadow-lg shadow-blue-500/50 dark:shadow-lg dark:shadow-blue-800/80 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2"
          >
            Click
          </button>

          <Slottest />
        </Hello>
      </main>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white p-4 w-screen">Footer Content</footer>
  </div>
</template>

<script>
import Hello from "./components/Hello.vue";
import Slottest from "./components/Slottest.vue";

export default {
  components: {
    Hello,
    Slottest,
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
