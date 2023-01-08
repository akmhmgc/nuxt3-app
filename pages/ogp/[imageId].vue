<script setup>
import heartFilled from "@/assets/heartFilled.png"
import heartOutline from "@/assets/heartOutline.png"
const route = useRoute();
const imageId = route.params.imageId;
const url = route.query.url;

useHead({
  title: 'OgpTest',
  meta: [
    { property: 'og:image', content: parseInt(imageId) > 10 ? heartFilled : heartOutline },
  ]
})

onMounted(() => {
  navigateTo(route.query.url, { external: true })
})

</script>
<template>
  <div>
    <h2>ogp sampleじゃ</h2>
    <h2>{{ imageId }}</h2>
    <h2>{{ url }}</h2>
  </div>
</template>

