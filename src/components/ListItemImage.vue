<template>
  <div>
    <img :src="userImage"/>
  </div>
</template>

<script>
export default {
  name: "ListItemImage",
  props: ["userImage"],
};
</script>

<style scoped>
img{
  width: 200px;
  height: 200px;
}
</style>
