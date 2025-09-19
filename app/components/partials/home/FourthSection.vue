<template>
  <section class="py-10 md:py-20">
    <div class="w-full max-w-[1304px] mx-auto px-4 pb-10">
      <div class="w-full flex justify-between items-end py-5">
        <div class="flex flex-col gap-4">
          <h4
            class="text-primary font-sf-pro-display text-base sm:text-[22px] font-bold"
          >
            Services
          </h4>
          <p
            class="text-septenary font-poppins font-semibold text-base sm:text-2xl md:text-4xl max-w-[453px] text-start"
          >
            Everything you need for your dog’s care
          </p>
        </div>

        <div class="flex items-center gap-4">
          <button
            @click="goToPrevious"
            :class="[
              'md:size-[52px] size-10 group border-2 cursor-pointer rounded-full flex items-center justify-center transition-all duration-200 hover:border-primary border-primary hover:bg-primary hover:text-secondary',
            ]"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              :class="[
                'size-6 transition-colors duration-200 text-primary group-hover:text-secondary',
              ]"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M15.75 19.5 8.25 12l7.5-7.5"
              />
            </svg>
          </button>
          <button
            @click="goToNext"
            :class="[
              'md:size-[52px] size-10 group border-2 cursor-pointer rounded-full flex items-center justify-center transition-all duration-200 hover:border-primary border-primary hover:bg-primary hover:text-secondary',
            ]"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              :class="[
                'size-6 rotate-180 transition-colors duration-200 text-primary group-hover:text-secondary',
              ]"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M15.75 19.5 8.25 12l7.5-7.5"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <Carousel
      ref="carouselRef"
      v-bind="carouselConfig"
      @slide-change="onSlideChange"
    >
      <Slide v-for="slide in slides" :key="slide.title">
        <div
          class="carousel__item items-start px-2 md:px-0 w-[370px]"
          :class="slide.width"
        >
          <ReadMoreCard
            :title="slide.title"
            :description="slide.description"
            :src="slide.src"
          />
        </div>
      </Slide>
    </Carousel>
  </section>
</template>

<script setup>
import { ref, computed } from "vue";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
import ReadMoreCard from "@/components/UI/ReadMoreCard.vue";
const carouselRef = ref(null);
const currentSlide = ref(0);

const carouselConfig = {
  wrapAround: true,
  gap: 15,
  itemsToShow: "auto",
};

const slides = [
  {
    src: "/assets/img/FourthSection/img1.png",
    title: "Dog Daycare",
    description:
      "Busy day ahead? Drop your dog off for a fun-filled day of play, cuddles, and companionship.",
    width: "md:w-[751px]",
  },
  {
    src: "/assets/img/FourthSection/img2.png",
    title: "Dog Boarding",
    description:
      "From cozy nights to playful days, we keep them active, loved, and cared for.",
    width: " md:w-[399px]",
  },
  {
    src: "/assets/img/FourthSection/img3.png",
    title: "Dog Walking",
    description:
      "Fresh air, exercise, and adventure — every pup deserves a good walk!",
    width: "md:w-[399px]",
  },
  {
    src: "/assets/img/FourthSection/img4.png",
    title: "Dog training",
    description:
      "Expect happy paws, wagging tails, and a content friend waiting for you when you get home.",
    width: "md:w-[760px]",
  },
  {
    src: "/assets/img/FourthSection/img5.png",
    title: "Pet Sitting (Dog & Cat)",
    description:
      "Sometimes the best care is in the comfort of home. We’ll visit your pets where they feel safest, keeping their routine as normal as possible.",
    width: "md:w-[751px]",
  },
];

const isFirstSlide = computed(() => currentSlide.value === 0);
const isLastSlide = computed(() => currentSlide.value === slides.length - 1);

const goToPrevious = () => {
  carouselRef.value.prev();
  currentSlide.value--;
};

const goToNext = () => {
  carouselRef.value.next();
  currentSlide.value++;
};

const onSlideChange = (index) => {
  currentSlide.value = index;
};
</script>

<style scoped>
</style>