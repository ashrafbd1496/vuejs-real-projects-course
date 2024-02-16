<template>
  <div class="maindiv border-2 border-teal-500 p-2 mb-4">
    
    <div class="header border-b border-solid border-black p-4">
      <slot name="slotHeader">I am Slot Header </slot>
    </div>
  
  <div class="body border-b border-solid border-black p-4">
    <slot/>
  </div>

  <div class="footer p-4">
    <slot name="slotFooter"> I am Slot Footer</slot>
  </div>

</div>
</template>

<script>
export default {
  name: "Hello",
  
};
</script>

<style scoped></style>
