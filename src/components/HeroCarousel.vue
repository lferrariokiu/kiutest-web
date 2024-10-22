<script setup>
const props = defineProps(['images']);
</script>

<template>
  <div v-for="image in images" :key="image.fields.title">
    {{ image.fields.title }}
    <img :src="image.fields.file.url" alt="" />
  </div>
</template>

<style scoped>
img {
  max-width: 350px;
}
</style>
