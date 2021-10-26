<template>
  <div class="relative flex flex-col items-top justify-center min-h-screen sm:items-center sm:pt-0 bg-green-600 text-white">
    <h1 class="text-xl font-bold mb-10">Contact</h1>
    <h2><i>Address</i></h2>
    <p class="max-w-xl">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tempore alias laudantium ab deleniti non harum minima illum accusamus similique sapiente.</p>
  </div>
</template>

<script>
export default {
  transition: 'flip'
}
</script>

<style>
.flip-enter-active {
  transition: transform 1s ease-out;
}

.flip-enter{
  /* opacity: 0; */
  transform: rotateY(180deg);
}
</style>
