<template>
  <Carousel v-bind="carouselConfig">
    <Slide v-for="item in items" :key="item.title">
      <div
        class="carousel__item w-full flex items-center gap-10 py-4 justify-between min-w-[300px] md:min-w-[654px]"
      >
        <span
          class="text-primary font-poppins font-medium text-6xl md:text-9xl"
        >
          {{ item.title }}
        </span>
        <svg
          width="51"
          height="49"
          viewBox="0 0 51 49"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M43.6488 40.1933C43.6536 44.6263 39.9637 48.1993 35.4859 48.0001C34.5649 47.9596 33.6821 47.756 32.8671 47.4172C30.7474 46.5359 28.4914 46.0297 26.1963 46.0319H25.5782C23.2146 46.034 20.878 46.5135 18.6977 47.4268C17.6675 47.8573 16.5238 48.0747 15.3237 48.0214C11.3228 47.8423 8.07154 44.5975 7.8842 40.5982C7.76133 37.9597 8.94717 35.5919 10.8491 34.0894C13.5821 31.9326 15.4911 28.8955 16.3923 25.5313C17.437 21.6237 19.9202 17.504 25.7394 17.4987C31.497 17.4923 33.9898 21.6258 35.0601 25.5377C35.986 28.9286 37.9963 31.9123 40.734 34.116C42.5099 35.545 43.6463 37.736 43.6488 40.1933Z"
            fill="#AF4C0F"
          />
          <path
            d="M12.757 23.0468C12.761 27.045 10.095 30.2888 6.80158 30.292C3.50887 30.2952 0.836573 27.0568 0.832524 23.0585C0.828581 19.0603 3.49448 15.8165 6.78719 15.8133C10.0799 15.8101 12.753 19.0486 12.757 23.0468Z"
            fill="#AF4C0F"
          />
          <path
            d="M23.9532 7.27629C23.9572 11.2745 21.2913 14.5193 17.9986 14.5215C14.7059 14.5257 12.0336 11.2862 12.0288 7.28801C12.0248 3.29085 14.6907 0.0460176 17.9842 0.0428209C21.2769 0.0396233 23.9492 3.27806 23.9532 7.27629Z"
            fill="#AF4C0F"
          />
          <path
            d="M50.6652 23.0067C50.6692 27.0049 48.0032 30.2497 44.7105 30.2529C41.4171 30.2561 38.7448 27.0177 38.7407 23.0195C38.7368 19.0212 41.4027 15.7764 44.6954 15.7732C47.9881 15.77 50.6613 19.0084 50.6652 23.0067Z"
            fill="#AF4C0F"
          />
          <path
            d="M39.4269 7.26253C39.4309 11.2608 36.765 14.5056 33.4715 14.5088C30.1788 14.512 27.5065 11.2735 27.5024 7.27532C27.4985 3.27709 30.1644 0.0333252 33.4571 0.0290623C36.7498 0.0258656 39.423 3.2643 39.4269 7.26253Z"
            fill="#AF4C0F"
          />
        </svg>
      </div>
    </Slide>
  </Carousel>
</template>

<script setup>
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
const carouselConfig = {
  wrapAround: true,
  autoplay: 3000,
  pauseAutoplayOnHover: true,
  gap: 40,
  itemsToShow: "auto",
  wrapAround: true,
};

const items = [
  {
    title: "Boarding",
  },
  {
    title: "Daycare",
  },
  {
    title: "Grooming",
  },
  {
    title: "Training",
  },
  {
    title: "Walking",
  },
  {
    title: "Medical",
  },
];
</script>

<style scoped>
</style>