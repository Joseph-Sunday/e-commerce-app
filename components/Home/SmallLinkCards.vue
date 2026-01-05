<template>
  <div
    class="Small-Card-Section bg-background flex justify-start items-center gap-3 mt-3 py-2 px-3 overflow-auto scroll-smooth no-scrollbar"
  >
    <div
      v-for="sc in smallCard"
      :key="sc.id"
      class="flex flex-col justify-center items-center"
    >
      <div>
        <img
          :src="sc.image"
          :alt="sc.title"
          class="small-card shadow-lg rounded-sm mb-3"
        />
      </div>
      <div>
        <p class="text-center text-gray-700 text-[13px] truncate">
          {{ sc.title }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  smallCard: {
    type: Array,
    required: true,
  },
});
</script>

<style scoped></style>
