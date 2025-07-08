<script setup>
const router = useRouter();
useHead({
  title: `${
    route.params.make ? toTitleCase(router.params.city) : "Cars"
  } in ${toTitleCase(router.params.city)}`,
  meta: [
    { name: "description", content: "Find your dream car with Car Trader" },
    { name: "viewport", content: "width=device-width, initial-scale=1" },
  ],
});

function toTitleCase(str) {
  return str.replace(/\w\S*/g, function (txt) {
    return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
  });
}
</script>

<template>
  <div>
    <div
      class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg:px-16 pb-16 w-3/5"
    >
      <div class="mt-32 flex">
        <CarSideBar />
        <NuxtPage />
      </div>
    </div>
  </div>
</template>
