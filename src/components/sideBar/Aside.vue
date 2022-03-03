<template>
  <div
    class="wrapper flex flex-col leftAside bg-white"
    :class="{ 'extended-wrapper': isShow }"
  >
    <aside-header :isShow="isShow" />
    <aside-main :isShow="isShow" />
    <aside-footer @showSideBar="showSideBar" />
  </div>
</template>

<script>
import AsideFooter from "./AsideFooter.vue";
import AsideHeader from "./AsideHeader.vue";
import AsideMain from "./AsideMain.vue";
export default {
  components: { AsideHeader, AsideMain, AsideFooter },
  data() {
    return {
      isShow: false,
    };
  },
  methods: {
    showSideBar(val) {
      this.isShow = val;
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
</style>
