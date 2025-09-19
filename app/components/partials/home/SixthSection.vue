<template>
  <section class="py-10 md:py-20 relative">
    <div class="absolute right-0 top-28 md:block hidden">
      <img src="/assets/img/steps.png" alt="" />
    </div>
    <div
      class="w-full max-w-[1321px] relative z-10 mx-auto px-4 pb-10 flex flex-col gap-10"
    >
      <div class="flex flex-col gap-4 items-center">
        <h4
          class="text-primary font-sf-pro-display text-base sm:text-[22px] font-bold"
        >
          Testimonials
        </h4>
        <p
          class="text-septenary font-poppins text-center font-semibold text-base sm:text-2xl md:text-4xl"
        >
          What people say about us
        </p>
      </div>

      <div
        class="w-full bg-septenary/5 rounded-2xl px-4 md:px-14 py-10 flex md:flex-row flex-col justify-between items-center gap-4"
      >
        <div class="flex items-center gap-2">
          <img src="/assets/icons/google.svg" alt="" class="size-[67px]" />
          <div class="flex items-start flex-col gap-px">
            <span class="text-septenary font-poppins font-semibold text-2xl">
              Google Rating
            </span>
            <div class="flex items-center gap-2">
              <span
                class="text-septenary font-poppins font-semibold sm:text-[28px] text-2xl"
              >
                4.8
              </span>
              <div class="flex items-center">
                <img
                  src="/assets/icons/star.svg"
                  alt=""
                  class="size-6"
                  v-for="i in 5"
                  :key="i"
                />
              </div>
              <span
                class="text-septenary font-sf-pro-display font-medium text-base sm:text-lg"
              >
                1,768 reviews
              </span>
            </div>
          </div>
        </div>

        <BaseButton class="text-lg font-semibold font-poppins text-secondary">
          Reviews on google
        </BaseButton>
      </div>

      <div class="w-full relative">
        <div
          class="absolute left-0 top-0 w-full h-full flex justify-center items-center"
        >
          <div
            class="w-full flex items-center gap-4 justify-between relative z-40"
          >
            <button
              @click="goToPrevious"
              :class="[
                '-ml-6 md:size-[52px] size-10 group border-2 cursor-pointer rounded-full flex items-center justify-center transition-all duration-200 hover:border-primary border-primary hover:bg-primary hover:text-secondary',
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
                '-mr-6 md:size-[52px] size-10 group border-2 cursor-pointer rounded-full flex items-center justify-center transition-all duration-200 hover:border-primary border-primary hover:bg-primary hover:text-secondary',
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
        <Carousel
          ref="carouselRef"
          v-bind="carouselConfig"
          @slide-change="onSlideChange"
        >
          <Slide v-for="slide in slides" :key="slide.image">
            <div class="carousel__item lg:w-[426px]">
              <div
                class="w-full overflow-hidden h-full min-h-[380px] rounded-lg bg-septenary/5 p-10"
              >
                <div
                  class="flex flex-col justify-between min-h-[380px] ga-p4 w-full"
                >
                  <div class="flex flex-col items-start gap-8">
                    <div class="flex items-center">
                      <img
                        src="/assets/icons/star.svg"
                        alt=""
                        class="size-6"
                        v-for="i in 5"
                        :key="i"
                      />
                      <span
                        class="text-septenary font-poppins font-semibold text-xl ml-2"
                      >
                        {{ slide.stars }}
                      </span>
                    </div>
                    <p
                      class="text-xl text-septenary font-sf-pro-display font-normal"
                    >
                      {{ slide.description }}
                    </p>
                  </div>

                  <div class="flex items-center gap-2">
                    <div
                      class="rounded-full size-14 bg-septenary/90 overflow-hidden"
                    >
                      <img
                        :src="slide.image"
                        alt=""
                        class="size-full object-cover"
                      />
                    </div>
                    <div class="flex flex-col gap-px">
                      <span
                        class="text-septenary font-poppins font-semibold text-xl"
                      >
                        {{ slide.name }}
                      </span>
                      <span
                        class="text-septenary font-sf-pro-display font-medium text-lg"
                      >
                        {{ slide.date }}
                      </span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </Slide>
        </Carousel>
      </div>
    </div>
  </section>
</template>

<script setup>
import BaseButton from "@/components/UI/BaseButton.vue";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
import LoopLine from "@/components/UI/LoopLine.vue";
const carouselRef = ref(null);
const currentSlide = ref(0);
const carouselConfig = {
  wrapAround: true,
  autoplay: 3000,
  itemsToShow: 3,
  pauseAutoplayOnHover: true,
  gap: 15,
  wrapAround: true,
  breakpoints: {
    0: {
      itemsToShow: 1,
    },
    768: {
      itemsToShow: 2,
    },
    1024: {
      itemsToShow: 3,
    },
  },
};

const slides = [
  {
    stars: 4.8,
    description:
      "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
    name: "Olivia Green",
    date: "2 days ago",
    image: "/assets/img/SixthSection/user2.png",
  },
  {
    stars: 4.9,
    description:
      "Cras in dui volutpat, porta lectus a, vehicula urna. Quisque vitae nunc sit amet lorem convallis vehicula.",
    name: "Liam Smith",
    date: "3 days ago",
    image: "/assets/img/SixthSection/user1.png",
  },
  {
    stars: 4.8,
    description:
      "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
    name: "Emma Brown",
    date: "5 days ago",
    image: "/assets/img/SixthSection/user3.png",
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