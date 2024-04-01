<template>
  <div>
    <img src="./assets/vue.svg" alt="" />
    <h1 class="mt-4">Vue http operations</h1>

    <button
      @click="getData()"
      href="#_"
      class="relative inline-flex items-center justify-start px-6 py-3 overflow-hidden font-medium transition-all border-1 border-teal-500 m-4 bg-white rounded hover:bg-white group"
    >
      <span
        class="w-48 h-48 rounded rotate-[-40deg] bg-teal-600 absolute bottom-0 left-0 -translate-x-full ease-out duration-500 transition-all translate-y-full mb-9 ml-9 group-hover:ml-0 group-hover:mb-32 group-hover:translate-x-0"
      ></span>
      <span
        class="relative w-full text-left text-black transition-colors duration-300 ease-in-out group-hover:text-white"
        >Get Data</span
      >
    </button>

    <ListWrapper :userList="userList" />
  </div>
</template>

<script>
import ListWrapper from "./components/ListWrapper.vue";

export default {
  name: "App",
  data() {
    return {
      userList: [],
      photos: [],
    };
  },
  components: {
    ListWrapper,
  },
  methods: {
    // getData() {
    //   fetch("https://jsonplaceholder.typicode.com/users")
    //     .then((response) => response.json())
    //     .then((data) => (this.userList = data));
    // },
    //fetch unsplsh data
    // getData() {
    //   fetch(url,
    //     "https://api.unsplash.com/photos?client_id=9wL0ngBpdebkJkC9DFYVBSECATYlCsLnWTiOnmgzTMo"
    //   ).then(response => response.blob())
    //     .then((response) => response.json())
    //     .then((data) => (this.userList = data));
    // },

    getData() {
      const url =
        "https://api.unsplash.com/photos?client_id=9wL0ngBpdebkJkC9DFYVBSECATYlCsLnWTiOnmgzTMo";

      fetch(url)
        .then((response) => response.json())
        .then((data) => {
          this.userList = data;
        })
        .catch((error) => {
          console.error("Error fetching data:", error);
        });
    },
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
