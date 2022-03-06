<template>
  <div
    class="wrapper flex flex-col leftAside bg-white"
    :class="{ 'extended-wrapper': isShow }"
  >
    <header class="flex items-center border-b border-gray-300 p-2 box-border">
      <div class="w-16">
        <img
          src="@/assets/img/logo.png"
          alt="logo"
          width="50px"
          height="50px"
        />
      </div>
      <div v-if="isShow">
        <h2>Strapi Website</h2>
        <p class="font-extralight">Workplace</p>
      </div>
    </header>
    <aside-menu :isShow="isShow" />
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
  </div>
</template>

<script>
import AsideMenu from "./AsideMenu.vue";
export default {
  components: { AsideMenu },
  data() {
    return {
      isShow: false,
    };
  },
  methods: {
    showSideBar() {
      this.isShow = !this.isShow;
    },
  },
};
</script>

<style scoped>
.leftAside {
  min-height: 100vh;
}
main {
  flex-grow: 10;
}
.wrapper {
  width: 70px;
}

.extended-wrapper {
  width: 300px;
}
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
