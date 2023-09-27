<template>
  <div>
    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const url = "https://fakestoreapi.com/products/" + id;

//fetch the product
const { data: product } = await useFetch(url, { key: id });
definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>
