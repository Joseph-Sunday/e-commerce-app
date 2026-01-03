<template>
  <div class="bg-background pt-3 pb-1">
    <div class="relative w-full px-2">
      <IconsSearch
        class="text-gray-500 absolute left-4 top-1/2 -translate-y-1/2 w-5 h-5"
      />
      <input
        type="text"
        placeholder="Search on Jshop"
        class="w-full rounded-lg bg-gray-200 text-gray-700 py-2 pl-9 pr-4 mt-1 text-sm focus:outline-none focus:ring-1 focus:ring-primary placeholder-gray-500"
      />
    </div>

    <div class="mt-3">
      <p class="bg-main text-white font-semibold text-[12px] pl-4 py-2">
        CALL TO ORDER: 07000000000, 02030000000
      </p>
    </div>

    <section class="">
      <Carousel />
    </section>
  </div>
</template>

<script setup></script>

<style scoped></style>
