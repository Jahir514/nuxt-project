<script setup>
const route = useRoute();
//custom composables
const { toTitleCase } = useUtilities();
useHead({
  title: `${
    route.params.make ? toTitleCase(route.params.make) : "Car"
  } in ${toTitleCase(route.params.city)}`,
});
definePageMeta({
  layout: "custom",
});
</script>
<template>
  <div>
    <div>
      <div class="mt-32 flex">
        <CarSideBar />
        <NuxtPage />
      </div>
    </div>
  </div>
</template>
