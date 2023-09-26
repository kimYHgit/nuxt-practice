<template>
  <div>
    <p>
      Prduct Details for <b>{{ id }}</b>
    </p>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>
