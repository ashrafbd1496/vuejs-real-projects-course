<script>

</script>

<template>
  <div class="header">
    <h2
      class="heading text-white bg-teal-500 text-2xl p-4 rounded-lg capitalize"
    >
      web dev with vue js real projects
    </h2>

    <svg
      xmlns="http://www.w3.org/2000/svg"
      fill="none"
      viewBox="0 0 24 24"
      strokeWidth="{1.5}"
      stroke="currentColor"
      className="w-6 h-6"
    >
      <path
        strokeLinecap="round"
        strokeLinejoin="round"
        d="m8.25 4.5 7.5 7.5-7.5 7.5"
      />
    </svg>

    <img src="/src/assets/logo-new.webp" alt="Logo" />
  </div>
</template>

<style>
.header {
  display: flex;
  flex-direction: row;
  width: 1000px;
  align-content: flex-start;
  align-items: center;
  justify-content: space-around;
  border: 1px solid gray;
}
.header > svg {
  width: 80px;
}
.header > img {
  width: 300px;
  height: auto;
  display: block;
  object-fit: contain;
}
</style>
