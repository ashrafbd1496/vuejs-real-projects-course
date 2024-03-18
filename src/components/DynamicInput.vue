<template>
  <div class="flex" v-for="(item, index) in userExp" :key="index">
    <div class="items-start mr-2 capitalize">
      <label :for="'company-' + index">Company</label>
      <input v-model="item.company" :id="'company-' + index" class="border-gray-500 ml-2 shadow appearance-none border rounded pl-2 mb-4" type="text" placeholder="Company">
    </div>
    <div class="capitalize">
      <label :for="'exp-' + index">Experience</label>
      <input v-model="item.exp" :id="'exp-' + index" class="border-gray-500 shadow appearance-none border ml-2 pl-2" type="number" placeholder="Experience">
    </div>
    <div class="ml-12">
      <button @click.prevent="addNewExp" class="btn btn-sm border border-gray-500 p-1">Add Exp</button>
    </div>
  </div>
</template>
<script>
export default {
  name: "DynamicInput",
  data(){
    return{
      userExp: [
        {
          company: '',
          exp: '',
        },
      ],
    };
  },
  methods:{
    addNewExp(){
      this.userExp.push({
        company:'',
        exp:'',
      });
    }
  }
};
</script>
<style scoped>
</style>
