<template>
  <div class="flex space-x-4 items-center justify-center w-full h-screen">
    <div>
      <nuxt-link class="bg-green-400 px-8 py-4 rounded-xl" to="/useFetch"
        >use fetch</nuxt-link
      >
    </div>
    <div>
      <NuxtLink class="bg-green-400 px-8 py-4 rounded-xl" to="/useLazyFetch"
        >use lazy fetch</NuxtLink
      >
    </div>
    <div>
      <NuxtLink to="/useAsyncData" class="bg-green-400 px-8 py-4 rounded-xl">
        use asyncData
      </NuxtLink>
    </div>
    <div>
      <NuxtLink to="useLazyAsyncData" class="bg-green-400 px-8 py-4 rounded-xl"
        >use lazyasyncData</NuxtLink
      >
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>