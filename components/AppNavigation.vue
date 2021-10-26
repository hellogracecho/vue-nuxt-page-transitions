<template>
  <header class="w-screen flex justify-center items-middle bg-purple-600">
    <ul class="max-w-xl flex">
      <li class="p-4 font-bold uppercase text-gray-300 hover:text-white">
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li class="p-4 font-bold uppercase text-gray-300 hover:text-white">
        <nuxt-link to="/about">About</nuxt-link>
      </li>
      <li class="p-4 font-bold uppercase text-gray-300 hover:text-white">
        <nuxt-link to="/contact">Contact</nuxt-link>
      </li>
    </ul>
    <button
      @click="menuOpened = !menuOpened"
      class="absolute z-20 top-0 right-0 p-4 bg-white"
    >
      <span v-text="menuOpened ? 'Close' : 'Open'"></span>
    </button>
    <app-menu-drawer :menuOpened="menuOpened"></app-menu-drawer>
  </header>
</template>

<script>
// import AppMenuDrawer from './AppMenuDrawer.vue'
export default {
  components: {
    // AppMenuDrawer,
  },
  data() {
    return {
      menuOpened: false,
    }
  },
}
</script>

<style scoped>
.nuxt-link-exact-active {
  @apply text-white underline;
}
</style>
