<template>
  <footer
    class="border-t border-gray-300 p-2 flex justify-between gap-x-2 items-center"
  >
    <div class="flex items-center gap-x-3">
      <div
        class="user bg-yellow-400 rounded-full w-1/2 flex items-center justify-center"
      >
        <img
          src="@/assets/img/user-ico.png"
          alt="user-ico"
          class="object-cover block"
          width="35px"
          height="35px"
        />
      </div>
      <p v-if="isShow">Adam Lambert</p>
    </div>
    <div>
      <button
        :class="{ 'rotate-arrow': isShow }"
        class="show-aside border border-gray-400 text-gray-500"
        @click="showSideBar()"
      >
        >
      </button>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      isShow: false,
    };
  },
  methods: {
    showSideBar() {
      this.isShow = !this.isShow;
      this.$emit("showSideBar", this.isShow);
    },
  },
};
</script>

<style scoped>
.user {
  height: 44px;
  min-width: 44px;
  max-width: 10%;
}
.show-aside {
  box-shadow: 0px 0px 7px 0px;
}
.rotate-arrow {
  transform: rotate(180deg);
}
</style>
