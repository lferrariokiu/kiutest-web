<script setup>
import { documentToHtmlString } from '@contentful/rich-text-html-renderer';


const props = defineProps(['item']);

</script>

<template>
  <div>
    <img :src="item.fields.hero.fields.file.url" alt="">
    {{ item.fields.title }}
    <div v-html="documentToHtmlString(item.fields.content)"></div>
  </div>
</template>

<style scoped>
img {
  max-width: 350px;
}
</style>
