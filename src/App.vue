<template>
  <div class="wrapper">
    <button
      type="button"
      class="bg-teal-500 text-white p-2"
      @click="showModal = true"
    >
      Open Modal
    </button>
    <teleport to="body">
      <div
        v-if="showModal"
        class="modal flex justify-center items-center fixed top-0 left-0 w-full h-full bg-teal-500 text-white"
      >
        <div
          class="modalContent text-white p-4 border border-dashed border-blue-500"
        >
          <h2 class="text-2xl font-extrabold">Modal Header</h2>
          <p>
            Modal Lorem ipsum dolor sit, amet consectetur adipisicing elit.
            Nulla dolor quidem voluptas, inventore veritatis unde
          </p>
          <button
            type="button"
            class="bg-white text-black p-2 mt-9 m-2"
            @click="showModal = false"
          >
            Modal Close
          </button>
        </div>
      </div>
    </teleport>
  </div>
</template>

<script>
//import DynamicA from "./components/DynamicA.vue";

export default {
  name: "App",
  components: {
    //DynamicA,
  },
  data() {
    return {
      showModal: false,
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
