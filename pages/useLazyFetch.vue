<template>
  <div>
    <div>use lazy fetch</div>
    <div v-if="pending">pending</div>
    <div v-else>
      {{ count }}
    </div>
  </div>
</template>

<script setup>
import axios from "axios";
const count = ref([]);
const { pending, data: products } = await useLazyFetch(
  axios.get("https://jsonplaceholder.ir/posts").then((res) => {
    count.value = res.data;
  })
);
</script>

<style>
</style>