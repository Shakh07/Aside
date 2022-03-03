<template>
  <main class="flex flex-col items-center mt-2">
    <div
      class="flex gap-x-4 items-center bg-gray-200 rounded p-2 w-11/12 mt-2"
      :class="{ 'icons-center': !isShow }"
    >
      <div>
        <content-icon class="svg-color h-6 w-8" />
      </div>
      <p v-if="isShow" class="text-indigo-600">Content</p>
    </div>
    <div class="mt-3 p-2 w-11/12 text-gray-500">
      <h2 v-if="isShow" class="text-sm font-bold mt-2">PLUGINS</h2>
      <div v-else class="border border-gray-300"></div>
      <ul
        class="list-none mt-4 p-1 flex flex-col gap-y-3"
        :class="{ 'icons-center': !isShow }"
      >
        <li class="flex items-center gap-x-6">
          <div>
            <builder-icon class="h-6 w-6" />
          </div>
          <p v-if="isShow">Builder</p>
        </li>
        <li class="flex items-center gap-x-6">
          <div>
            <media-icon class="h-6 w-6" />
          </div>
          <p v-if="isShow">Media Library</p>
        </li>
        <li class="flex items-center gap-x-6">
          <div>
            <documentation-icon class="h-6 w-6" />
          </div>
          <p v-if="isShow">Documentation</p>
        </li>
      </ul>
      <h2 v-if="isShow" class="text-sm font-bold mt-4">GENERAL</h2>
      <div v-else class="border border-gray-300 mt-4"></div>
      <ul
        class="list-none mt-4 p-1 flex flex-col gap-y-3"
        :class="{ 'icons-center': !isShow }"
      >
        <li class="flex items-center gap-x-6">
          <div>
            <plugins-icon class="h-6 w-6" />
          </div>
          <p v-if="isShow">Plugins</p>
        </li>
        <li class="flex items-center gap-x-6">
          <div>
            <market-icon class="h-6 w-6" />
          </div>
          <p v-if="isShow">Marketplace</p>
        </li>
        <li class="flex items-center gap-x-6">
          <div>
            <settings-icon class="h-6 w-6" />
          </div>
          <p v-if="isShow">Settings</p>
        </li>
      </ul>
    </div>
  </main>
</template>

<script>
import BuilderIcon from "../icons/BuilderIcon.vue";
import ContentIcon from "../icons/ContentIcon.vue";
import DocumentationIcon from "../icons/DocumentationIcon.vue";
import MarketIcon from "../icons/MarketIcon.vue";
import MediaIcon from "../icons/MediaIcon.vue";
import PluginsIcon from "../icons/PluginsIcon.vue";
import SettingsIcon from "../icons/SettingsIcon.vue";
export default {
  components: {
    ContentIcon,
    BuilderIcon,
    MediaIcon,
    DocumentationIcon,
    PluginsIcon,
    MarketIcon,
    SettingsIcon,
  },
  props: {
    isShow: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style scoped>
.svg-color {
  fill: rgb(70, 70, 229);
}
.icons-center {
  align-items: center;
  justify-content: center;
}
</style>
