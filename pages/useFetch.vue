<template>
  <div>
    fetch

    <div>{{ count }}</div>
  </div>
</template>

<script setup>
import axios from "axios";
const count = ref([]);
const { data: products } = useFetch(
  axios.get("https://jsonplaceholder.ir/posts").then((res) => {
    count.value = res.data;
  })
);
</script>

<style>
</style>