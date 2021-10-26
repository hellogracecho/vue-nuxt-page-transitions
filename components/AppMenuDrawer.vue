<template>
  <transition name="menu">
    <div
      v-if="menuOpened"
      class="menudrawer absolute z-20 top-12 right-0 bg-white p-4"
    >
      <nuxt-link to="/" class="text-green-600 hover:text-blue-600"
        >Home</nuxt-link
      >
      <nuxt-link to="/about" class="text-green-600 hover:text-blue-600"
        >About</nuxt-link
      >
      <nuxt-link to="/contact" class="text-green-600 hover:text-blue-600"
        >Contact</nuxt-link
      >
    </div>
  </transition>
</template>

<script>
export default {
  props: {
    menuOpened: {
      type: Boolean,
      default: true,
    },
  },
}
</script>

<style scoped>
.menu-enter-active {
  transition: all 0.3s ease;
}
.menu-leave-active {
  transition: all 0.25s cubic-bezier(1, 0.5, 0.8, 1);
}

.menu-enter,
.menu-leave-to {
  transform: scale(0.9);
  transform-origin: '100% 0%';
  opacity: 0;
}
</style>
