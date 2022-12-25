<script setup>
const { cars } = useCars()
const route = useRoute()
useHead({
  title: route.params.name
})


definePageMeta({
  layout: "custom"
})

const car = computed(() => {
  return cars.find((car) => {
    return car.id === parseInt(route.params.id)
  })
})

</script>
<template>
  <div v-if="car">
    <CarDetailHero :car="car" />
    <CarDetailAttributes :features="car.features" />
    <CarDetailDescription :description="car.description" />
    <CarDetailContact />
  </div>
</template>
