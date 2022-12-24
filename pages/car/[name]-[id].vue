<script setup>
const route = useRoute()
useHead({
  title: route.params.name
})

definePageMeta({
  layout: "custom"
})

</script>
<template>
  <CarDetailHero />
  <CarDetailAttributes />
  <CarDetailDescription />
  <CarDetailContact />
</template>
