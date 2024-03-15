<template>
  <div class="main-wrapper flex">
    <div class="wrapper">
      <section
        class="max-w-xl p-6 mx-auto bg-indigo-600 rounded-md shadow-md dark:bg-gray-800 mt-20"
      >
        <h1 class="text-xl font-bold text-white capitalize dark:text-white">
          Account settings
        </h1>
        <form @submit.prevent="submitForm">
          <div class="grid grid-cols-1 gap-6 mt-4 sm:grid-cols-2">
            <div>
              <label class="text-white dark:text-gray-200" for="username"
                >Username</label
              >
              <input
                v-model="user.name"
                id="username"
                type="text"
                class="block w-full px-4 py-2 mt-2 text-gray-700 bg-white border border-gray-300 rounded-md dark:bg-gray-800 dark:text-gray-300 dark:border-gray-600 focus:border-blue-500 dark:focus:border-blue-500 focus:outline-none focus:ring"
              />
            </div>

            <div>
              <label class="text-white dark:text-gray-200" for="emailAddress"
                >Email Address</label
              >
              <input
                v-model="user.email"
                id="emailAddress"
                type="email"
                class="block w-full px-4 py-2 mt-2 text-gray-700 bg-white border border-gray-300 rounded-md dark:bg-gray-800 dark:text-gray-300 dark:border-gray-600 focus:border-blue-500 dark:focus:border-blue-500 focus:outline-none focus:ring"
              />
            </div>

            <div>
              <label class="text-white dark:text-gray-200" for="password"
                >Password</label
              >
              <input
                id="password"
                type="password"
                class="block w-full px-4 py-2 mt-2 text-gray-700 bg-white border border-gray-300 rounded-md dark:bg-gray-800 dark:text-gray-300 dark:border-gray-600 focus:border-blue-500 dark:focus:border-blue-500 focus:outline-none focus:ring"
              />
            </div>

            <div>
              <label
                class="text-white dark:text-gray-200"
                for="passwordConfirmation"
                >Password Confirmation</label
              >
              <input
                id="passwordConfirmation"
                type="password"
                class="block w-full px-4 py-2 mt-2 text-gray-700 bg-white border border-gray-300 rounded-md dark:bg-gray-800 dark:text-gray-300 dark:border-gray-600 focus:border-blue-500 dark:focus:border-blue-500 focus:outline-none focus:ring"
              />
            </div>
            <div class="">
              <h2 class="text-white dark:text-gray-200">Gender</h2>
              <div v-for="item in gender" :key="item.id">
                <input
                  v-model="user.gender"
                  id="football"
                  type="radio"
                  :value="item.name"
                />
                <label for="football" class="text-white pr-2.5">{{
                  item.name
                }}</label>
              </div>
            </div>
            <div>
              <label
                class="text-white dark:text-gray-200"
                for="passwordConfirmation"
                >Country</label
              >
              <select
                v-model="user.country"
                id="country"
                name="country"
                class="selected block w-full px-4 py-2 mt-2 text-gray-700 bg-white border border-gray-300 rounded-md dark:bg-gray-800 dark:text-gray-300 dark:border-gray-600 focus:border-blue-500 dark:focus:border-blue-500 focus:outline-none focus:ring"
              >
                <option
                  v-for="item in getCountries"
                  :key="item.id"
                  :value="item.id"
                >
                  {{ item.name }}
                </option>
              </select>
            </div>
            <div class="hobbies">
              <h2 class="text-white dark:text-gray-200">Hobbies</h2>
              <div v-for="item in hobbies" :key="item.id">
                <label for="football" class="text-white pr-2.5">{{
                  item.name
                }}</label>
                <input
                  v-model="user.hobbies"
                  id="football"
                  type="checkbox"
                  :value="item.name"
                />
              </div>
            </div>
            <div>
              <label
                class="text-white dark:text-gray-200"
                for="passwordConfirmation"
                >Date</label
              >
              <input
                id="date"
                type="date"
                class="block w-full px-4 py-2 mt-2 text-gray-700 bg-white border border-gray-300 rounded-md dark:bg-gray-800 dark:text-gray-300 dark:border-gray-600 focus:border-blue-500 dark:focus:border-blue-500 focus:outline-none focus:ring"
              />
            </div>
            <div>
              <label
                class="text-white dark:text-gray-200"
                for="passwordConfirmation"
                >Address</label
              >
              <textarea
                v-model="user.address"
                id="textarea"
                type="textarea"
                class="block w-full px-4 py-2 mt-2 text-gray-700 bg-white border border-gray-300 rounded-md dark:bg-gray-800 dark:text-gray-300 dark:border-gray-600 focus:border-blue-500 dark:focus:border-blue-500 focus:outline-none focus:ring"
              ></textarea>
            </div>
            <div>
              <label class="block text-sm font-medium text-white">
                Image
              </label>
              <div
                class="mt-1 flex justify-center px-6 pt-5 pb-6 border-2 border-gray-300 border-dashed rounded-md"
              >
                <div class="space-y-1 text-center">
                  <svg
                    class="mx-auto h-12 w-12 text-white"
                    stroke="currentColor"
                    fill="none"
                    viewBox="0 0 48 48"
                    aria-hidden="true"
                  >
                    <path
                      d="M28 8H12a4 4 0 00-4 4v20m32-12v8m0 0v8a4 4 0 01-4 4H12a4 4 0 01-4-4v-4m32-4l-3.172-3.172a4 4 0 00-5.656 0L28 28M8 32l9.172-9.172a4 4 0 015.656 0L28 28m0 0l4 4m4-24h8m-4-4v8m-12 4h.02"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                  <div class="flex text-sm text-gray-600">
                    <label
                      for="file-upload"
                      class="relative cursor-pointer bg-white rounded-md font-medium text-indigo-600 hover:text-indigo-500 focus-within:outline-none focus-within:ring-2 focus-within:ring-offset-2 focus-within:ring-indigo-500"
                    >
                      <span class="block"
                        @click="$refs.myFileInput.click()"
                        
                        >{{file?.name ? "Change File" : "Select File"}}</span
                      >
                      <input
                      
                        @change="onFileChange"
                        ref="myFileInput"
                        id="file-upload"
                        name="file-upload"
                        type="file"
                        class="sr-only"
                      />
                      <span v-if="file?.name">{{file.name}}</span>
                    </label>
                    <p class="pl-1 text-white">or drag and drop</p>
                  </div>
                  <p class="text-xs text-white">PNG, JPG, GIF up to 10MB</p>
                </div>
              </div>
            </div>
          </div>

          <div class="flex justify-end mt-6">
            <button
              class="px-6 py-2 leading-5 text-white transition-colors duration-200 transform bg-pink-500 rounded-md hover:bg-pink-700 focus:outline-none focus:bg-gray-600"
            >
              Save
            </button>
          </div>
        </form>
      </section>
    </div>
    <div class="wrapper max-w-xl p-6 mt-20 mx-auto">
      <p>User info: {{ user }}</p>
      <p>User Country: {{ getCountryNameById(user.country) }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "Form",
  data() {
    return {
      countries: [
        { id: 1, name: "Saudi Arabia" },
        { id: 2, name: "Filistin" },
        { id: 3, name: "Egypt" },
      ],
      hobbies: [
        { id: 1, name: "Football" },
        { id: 2, name: "Basketball" },
        { id: 3, name: "Volleyball" },
      ],
      gender: [
        { id: 1, name: "Male" },
        { id: 2, name: "Female" },
        { id: 3, name: "Other" },
      ],
      user: {
        name: "",
        email: "",
        country: 1,
        address: "",
        hobbies: [],
        gender: [],
        file:"",
       
      },
      file: {},
    };
  },
  methods: {
    getCountryNameById(id) {
      return this.countries.find((item) => item.id === id).name;
    },
    submitForm(){
      this.user={
        name: "",
        email: "",
        country: 1,
        address: "",
        hobbies: [],
        gender: [],
        file:[],
       
      };
      this.file=[]
    },
    onFileChange(e) {
      this.user.file={
        name:e.target.files[0].name,
        size:e.target.files[0].size,
        type:e.target.files[0].type
      },
      console.log(e.target.files);
      this.file={name:e.target.files[0].name}
    },
  },
  computed: {
    getCountries() {
      return this.countries;
    },
  },
};
</script>
<style scoped></style>
