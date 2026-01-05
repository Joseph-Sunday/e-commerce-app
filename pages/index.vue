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
        <p class="bg-cta text-white font-semibold text-[12px] pl-4 py-2">
          CALL TO ORDER: 07000000000, 02030000000
        </p>
      </div>

      <section class="Home-carousel">
        <HomeCarousel />
      </section>
    </div>

    <section class="Home-smallLinkCards">
      <HomeSmallLinkCards :smallCard="smallCardDetails" />
    </section>

    <section class="Flash-sales">
      <div class="bg-background mt-3">
        <div class="bg-cta text-white flex justify-around items-center gap-10">
          <div class="py-2">
            <h4 class="text-white font-extrabold text-[13px]">FLASH SALES</h4>
            <p class="text-[13px] font-heading">
              Time Left:
              <span class="font-semibold">{{ " " }} 00h : 56m : 32s</span>
            </p>
          </div>
          <div class="font-bold text-[13px]">SEE ALL</div>
        </div>

        <FlashSalesCard :product="productDetails" />
      </div>
    </section>
  </div>
</template>

<script setup>
import FlashSalesCard from "~/components/Home/FlashSalesCard.vue";

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
    title: "Shop and Earn",
    image: "images/shopAndEarn.png",
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
    image: "images/gameDeals.png",
  },
  {
    id: 9,
    title: "Unlock Your Deal",
    image: "images/tenPercentOff.png",
  },
  {
    id: 10,
    title: "Fulfilled By Jshop",
    image: "images/powerbanks.png",
  },
];

const productDetails = [
  {
    id: 1,
    image: "/images/powerbanks.png",
    title: "20000mAh Dual...",
    price: "N 14,450",
    quantity: "10 items left",
    progress: 10,
    discount: "-28%",
  },
  {
    id: 2,
    image: "/images/powerbanks.png",
    title: "20000mAh Dual...",
    price: "N 14,450",
    quantity: "67 items left",
    progress: 67,
    discount: "-44%",
  },
  {
    id: 3,
    image: "/images/powerbanks.png",
    title: "20000mAh Dual...",
    price: "N 14,450",
    quantity: "80 items left",
    progress: 80,
    discount: "-12%",
  },
  {
    id: 4,
    image: "/images/powerbanks.png",
    title: "20000mAh Dual...",
    price: "N 14,450",
    quantity: "28 items left",
    progress: 28,
    discount: "-9%",
  },
  {
    id: 5,
    image: "/images/powerbanks.png",
    title: "20000mAh Dual...",
    price: "N 14,450",
    quantity: "58 items left",
    progress: 58,
    discount: "-23%",
  },
];
</script>

<style scoped></style>
