<template>
  <div>
    <div class="bg-background Hero-section pt-3">
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

    <section class="mb-3">
      <HomeCarousel />
    </section>
    </div>
    

    <section class="">
      <HomeSmallLinkCards :smallCard="smallCardDetails" />
    </section>
  </div>
</template>

<script setup>
  const smallCardDetails = [
  {
    id: 1,
    title: "Awoof Deals",
    image: "images/awoofDeals.png",
  },
  {
    id: 2,
    title: "Up to 80% Off",
    image: "images/clearance.png",
  },
  {
    id: 3,
    title: "Awoof Deals",
    image: "images/awoofDeals.png",
  },
  {
    id: 4,
    title: "Kids, Baby and More",
    image: "images/kidsAndBabys.png",
  },
  {
    id: 5,
    title: "Unbeatable offers",
    image: "images/twoForOne.png",
  },
  {
    id: 6,
    title: "Send Packages",
    image: "images/delivery.png",
  },
  {
    id: 7,
    title: "Groceries",
    image: "images/groceries.png",
  },
  {
    id: 8,
    title: "Deals Reloaded",
    image: "images/gameSales.png",
  },
  {
    id: 9,
    title: "Unlock Your Deal",
    image: "images/awoofDeals.png",
  },
  {
    id: 10,
    title: "Fulfilled By Jshop",
    image: "images/powerbanks.png",
  },
];
</script>

<style scoped></style>
