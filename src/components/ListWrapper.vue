<template>
  <div>
    <ul class="grid grid-cols-4 gap-8">
     <ListItem v-for="item in userList" :key="item.id" :userItem="item"/>
    </ul>
  </div>  
</template>
<script>
import ListItem from "./ListItem.vue";

export default {
  name: "ListWrapper",

  components:{
    ListItem,
  },
  props:["userList"],
};
</script>

<style scoped>

</style>
