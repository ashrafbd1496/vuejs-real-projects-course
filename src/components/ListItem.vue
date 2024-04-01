<template>
  <div class="object-cover">
    <li class="max-w-xs rounded overflow-hidden shadow-lg">
      <ListItemImage :userImage="userItem.urls.small" />
      <div class="px-6 py-4">
        <ListItemTitle :userName="userItem.user.username" />
        <ListItemBody :userBody="userItem.id" />
        <ListItemBody :userBody="userItem.created_at" />
      </div>
    </li>
   
  </div>
</template>

<script>
import ListItemImage from "./ListItemImage.vue";
import ListItemTitle from "./ListItemTitle.vue";
import ListItemBody from "./ListItemBody.vue";

export default {
  name: "ListItem",
  components: {
    ListItemImage,
    ListItemTitle,
    ListItemBody,
  },
  props:[
    "userItem",

  ],
};
</script>
<style scoped> 
li {
  transition: all 0.9s;
}

li:hover {
  transform: scale(1.1);
}
</style>
