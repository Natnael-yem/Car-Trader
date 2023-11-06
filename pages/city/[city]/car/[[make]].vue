<script setup>
const route = useRoute()
const cars  = await useFetchCars(route.params.city, {
  minPrice: route.query.minPrice,
  maxPrice: route.query.maxPrice,
  make: route.params.make
});

</script>

<template>
  <div>
    
    <CarCards v-if="cars.length" :cars="cars"/>
    <h1 v-else >No Cars found with this Filters</h1>
  </div>
</template>
 