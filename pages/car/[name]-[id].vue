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

if (!car.value) {
  throw createError({
    statusCode: 404,
    message: `Car with id of ${route.params.id} does not exist`
  })
}

</script>
<template>
  <div>
    <CarDetailHero :car="car" />
    <CarDetailAttributes :features="car.features" />
    <CarDetailDescription :description="car.description" />
    <CarDetailContact />
  </div>
</template>
