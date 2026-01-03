<template>
  <Swiper
    :modules="[Autoplay, Pagination]"
    :slides-per-view="1.2"
    :space-between="16"
    :loop="true"
    :autoplay="{
      delay: 5000,
      disableOnInteraction: false,
    }"
    :pagination="{ clickable: true }"
    class="w-full"
    :breakpoints="{
      640: { slidesPerView: 2 },
      1024: { slidesPerView: 3 },
    }"
  >
    <SwiperSlide
      v-for="c in carousel"
      :key="c.id"
      class="bg-white rounded-lg shadow mt-3 overflow-hidden"
    >
      <div class="cursor-grab w-full rounded-lg shadow">
        <img :src="c.image" :alt="c.name" class="w-full max-h-[155px]" />
      </div>
    </SwiperSlide>
  </Swiper>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";

import "swiper/css";
import "swiper/css/pagination";

const carousel = [
  {
    id: 1,
    image: "/images/gameSales.png",
    name: "Games Sales",
  },
  {
    id: 2,
    image: "/images/shirtSales.png",
    name: "Shirt sales",
  },
  {
    id: 3,
    image: "/images/furniture.png",
    name: "Furniture",
  },
  {
    id: 4,
    image: "/images/fashion.png",
    name: "Fashion",
  },
];
</script>

<style scoped></style>
