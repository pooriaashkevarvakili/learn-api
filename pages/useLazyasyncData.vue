<template>
  <div>
    useLazyasyncData
    <div v-if="pending"></div>
    <div v-else>{{ count }}</div>
  </div>
</template>

<script setup>
import axios from "axios";
const count = ref([]);
const { pending, data: products } = useLazyAsyncData("count", () =>
  $fetch(
    axios.get("https://jsonplaceholder.ir/posts").then((res) => {
      count.value = res.data;
    })
  )
);
</script>

<style>
</style>