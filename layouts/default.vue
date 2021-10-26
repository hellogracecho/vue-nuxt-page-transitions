<template>
  <div>
    <app-navigation />
    <nuxt />
  </div>
</template>
<script>
import AppNavigation from "~/components/AppNavigation.vue";

export default {
  components: {
    AppNavigation,
  },
};
</script>

<style>
/* Page simple fade in out */
/* .page-enter-active,
.page-leave-active {
  transition: all 0.25s ease;
}

.page-enter,
.page-leave-active {
  opacity: 0;
  transform: translateZ(s0);
  backface-visibility: hidden;
} */

/* Page across in and out */
.page-enter-active {
  animation: acrossIn .45s ease-out both;
}

.page-leave-active {
  animation: acrossOut .65s ease-in both;
}

@keyframes acrossIn {
  0% {
    transform: translate3d(-100%, 0, 0);
  }
  100% {
    transform: translate3d(0, 0, 0);
  }
}

@keyframes acrossOut {
  0% {
    transform: translate3d(0, 0, 0);
  }
  100% {
    transform: translate3d(100%, 0, 0);
  }
}
</style>
