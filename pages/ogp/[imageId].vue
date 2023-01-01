<script setup>
import heartFilled from "@/assets/heartFilled.png"
import heartOutline from "@/assets/heartOutline.png"
const route = useRoute();
const imageId = route.params.imageId

useHead({
  title: 'OgpTest',
  meta: [
    { property: 'og:image', content: parseInt(imageId) > 10 ? heartFilled : heartOutline },
  ]
})
</script>
<template>
  <div>
    <h2>ogp sampleじゃ</h2>
    <h2>{{ imageId }}</h2>
  </div>
</template>
