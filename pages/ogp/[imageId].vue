<script setup>
const route = useRoute();
const imageId = route.params.imageId;
const url = route.query.url;

useHead({
  title: 'OgpTest',
  meta: [
    { property: 'og:image', content: 'https://images.keizai.biz/abeno_keizai/headline/1551938569_photo.jpg' },
  ]
})

definePageMeta({
  layout: false
})

onMounted(() => {
  navigateTo(route.query.url, { external: true })
})

</script>
<template>
  <div>
  </div>
</template>

