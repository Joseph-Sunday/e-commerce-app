<template>
  <div
    class="bg-background flex justify-start items-center gap-3 mt-3 py-2 px-3 overflow-auto scroll-smooth no-scrollbar"
  >
    <div v-for="sc in smallCard" :key="sc.id" class="">
      <div>
        <img
          :src="sc.image"
          :alt="sc.title"
          class="small-card shadow-lg rounded-sm mb-3"
        />
      </div>
      <div>
        <p class="text-center text-gray-700 text-[13px] break">
          {{ sc.title }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  smallCard: [
    {
      type: Object,
      required: true,
    },
  ],
});
</script>

<style scoped></style>
