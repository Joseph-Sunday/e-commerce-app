<template>
  <div>
    <div
      class="flash-sales-card pl-3 py-4 flex justify-start items-center gap-3 overflow-auto no-scrollbar"
    >
      <div
        class="relative card p-3 flex flex-col justify-center items-center gap-5"
        v-for="p in product"
        :key="p.id"
      >
        <div
          class="absolute text-cta font-heading text-[12px] bg-background px-2 rounded-sm top-4 left-[6rem]"
        >
          {{ p.discount }}
        </div>
        <div class="image">
          <img :src="p.image" :alt="p.title" class="min-w-[130px] h-full" />
        </div>
        <div>
          <p class="font-extralight self-start truncate">{{ p.title }}</p>
          <p class="font-heading font-semibold self-start">
            {{ p.price }}
          </p>
        </div>
        <div class="progress-bar self-start w-full">
          <p class="font-extralight text-sm mb-1">{{ p.quantity }}</p>
          <div class="h-2 w-full bg-gray-200 rounded-full overflow-hidden">
            <div
              class="h-full bg-blue-400 rounded-full transition-all duration-500"
              :style="{ width: getProgress(p.progress) + '%' }"
            ></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  product: {
    type: Array,
    required: true,
  },
});

const getProgress = (progress, total = 100) => {
  return Math.min((progress / total) * 100, 100);
};
</script>

<style scoped></style>
