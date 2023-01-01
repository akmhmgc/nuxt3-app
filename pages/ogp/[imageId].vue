<script setup>
import heartFilled from "@/assets/heartFilled.png"
const route = useRoute();

useHead({
  title: 'OgpTest',
  meta: [
    { property: 'og:image', content: heartFilled },
  ]
})
</script>
<template>
  <div>
    <h2>ogp sampleじゃ</h2>
    <h2>{{ route.params.imageId }}</h2>
    <h2>{{ route.fullPath }}</h2>
    <h2>{{ route.path }}</h2>
  </div>
</template>
