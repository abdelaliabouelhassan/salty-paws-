<template>
  <section class="pt-10 md:pt-20">
    <div
      class="w-full max-w-[1119px] px-4 mx-auto flex flex-col items-center gap-5 pb-10"
    >
      <h4
        class="text-primary font-sf-pro-display text-base sm:text-[22px] font-bold"
      >
        Our story
      </h4>
      <p
        class="text-septenary font-poppins text-lg sm:text-2xl md:text-4xl font-semibold text-center"
      >
        We treat every dog like part of our family, creating a safe, caring, and
        stimulating environment that supports both their physical health and
        emotional well-being.
      </p>
    </div>

    <Carousel v-bind="carouselConfig">
      <Slide v-for="slide in slides" :key="slide.src">
        <div
          class="carousel__item w-full max-w-[370px] md:max-w-[550px] h-[525px]"
        >
          <div class="w-full h-full overflow-hidden rounded-lg">
            <img
              :src="slide.src"
              alt="slide"
              class="w-full h-full object-cover"
            />
          </div>
        </div>
      </Slide>
    </Carousel>
  </section>
</template>

<script setup>
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
const carouselConfig = {
  wrapAround: true,
  autoplay: 2000,
  pauseAutoplayOnHover: true,
  gap: 15,
  itemsToShow: "auto",
  wrapAround: true,
};

const slides = [
  {
    src: "/assets/img/FirstSection/img1.png",
  },
  {
    src: "/assets/img/FirstSection/img2.png",
  },
  {
    src: "/assets/img/FirstSection/img3.png",
  },
  {
    src: "/assets/img/FirstSection/img4.png",
  },
  {
    src: "/assets/img/FirstSection/img5.png",
  },
];
</script>

<style scoped>
</style>