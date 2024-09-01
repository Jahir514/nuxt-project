<script setup>
const route = useRoute();
const { toTitleCase } = useUtilities();
useHead({
  title: toTitleCase(route.params.carName),
});
definePageMeta({
  layout: "custom",
});
</script>

<template>
  <div>
    <div>
      <!-- CAR DETAIL PAGE -->

      <CarDetailsHero />
      <CarDetailsAttribute />
      <CarDetailsDescription />
      <CarDetailsContact />

      <!-- CAR DETAIL PAGE   -->
    </div>
  </div>
</template>
