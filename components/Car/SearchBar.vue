<script setup>
const city = ref("");
const cityError = ref(false);

const handleSearch = () => {
  if (!city.value) {
    return (cityError.value = true);
  }
  navigateTo(`/city/${city.value}/car`);
};
</script>

<template>
  <div
    class="
      font-serif
      w-[300px]
      text-1xl
      rounded-full
      bg-white
      flex
      justify-between
      overflow-hidden
      drop-shadow-2xl
      mx-auto
    "
  >
    <input
      type="text"
      class="py-1 px-2.5  text-1xl rounded-full focus:outline-none"
      :class="cityError ? 'border-red-500 border' : ''"
      placeholder="Search by Location..."
      v-model="city"
    />
    <button class="bg-sky-500 px-3 text-white" @click="handleSearch">
      Search
    </button>
  </div>
</template>