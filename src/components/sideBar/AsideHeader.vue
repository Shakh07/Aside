<template>
  <header class="flex items-center border-b border-gray-300 p-2 box-border">
    <div class="w-16">
      <img src="@/assets/img/logo.png" alt="logo" width="50px" height="50px" />
    </div>
    <div v-if="isShow">
      <h2>Strapi Website</h2>
      <p class="font-extralight">Workplace</p>
    </div>
  </header>
</template>

<script>
export default {
  props: {
    isShow: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style></style>
