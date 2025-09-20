<template>
  <section class="py-10 md:py-20" id="services">
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
            :openModal="() => readMoreModal.openModal(slide.details)"
          />
        </div>
      </Slide>
    </Carousel>
  </section>
  <ReadMoreModal ref="readMoreModal" />
</template>

<script setup>
import { ref, computed } from "vue";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
import ReadMoreCard from "@/components/UI/ReadMoreCard.vue";
const carouselRef = ref(null);
const currentSlide = ref(0);
import ReadMoreModal from "@/components/UI/ReadMoreModal.vue";
const readMoreModal = ref(null);
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
    details: {
      title: "Dog Daycare",
      description: `Busy day ahead? Drop your dog off for a fun-filled day of play, cuddles, and companionship. <br> <br> Our daycare provides a safe space where they can burn energy, make friends, and enjoy structured activities — so when you pick them up, they’re happy and relaxed.`,
      included: ["Playtime & Exercise", "Socialization", "Meals/snacks"],
      durationOptions: "Half day / Full day",
      price: "25.00€",
      images: [
        "/assets/img/FourthSection/img6.png",
        "/assets/img/FourthSection/img1.png",
        "/assets/img/FourthSection/img5.png",
      ],
    },
  },
  {
    src: "/assets/img/FourthSection/img2.png",
    title: "Dog Boarding",
    description:
      "From cozy nights to playful days, we keep them active, loved, and cared for.",
    width: " md:w-[399px]",
    details: {
      title: "Dog Boarding",
      description: `Busy day ahead? Drop your dog off for a fun-filled day of play, cuddles, and companionship. <br> <br> Our daycare provides a safe space where they can burn energy, make friends, and enjoy structured activities — so when you pick them up, they’re happy and relaxed.`,
      included: ["Playtime & Exercise", "Socialization", "Meals/snacks"],
      durationOptions: "Half day / Full day",
      price: "25.00€",
      images: [
        "/assets/img/FourthSection/img1.png",
        "/assets/img/FourthSection/img7.png",
        "/assets/img/FourthSection/img8.png",
      ],
    },
  },
  {
    src: "/assets/img/FourthSection/img3.png",
    title: "Dog Walking",
    description:
      "Fresh air, exercise, and adventure — every pup deserves a good walk!",
    width: "md:w-[399px]",
    details: {
      title: "Dog Walking",
      description: `Fresh air, exercise, and adventure — every pup deserves a good walk! Whether your dog loves a gentle stroll or a more energetic outing, we make sure their walk is safe, fun, and tailored to their needs. <br> <br> Expect happy paws, wagging tails, and a content friend waiting for you when you get home.`,
      included: [
        "Tailored walks to match your dog’s energy",
        "Water breaks",
        "Playtime & Plenty of sniffs along the way",
      ],
      durationOptions: "30 minutes / 60 minutes",
      price: "15.00€",
      images: [
        "/assets/img/FourthSection/img3.png",
        "/assets/img/FourthSection/img9.png",
        "/assets/img/FourthSection/img10.png",
      ],
    },
  },
  {
    src: "/assets/img/FourthSection/img4.png",
    title: "Dog training",
    description:
      "Expect happy paws, wagging tails, and a content friend waiting for you when you get home.",
    width: "md:w-[760px]",
    details: {
      title: "Dog Training",
      description: `Do you have a detailed process to add? not really, i usually create a plan acoording too what the costumer would like fix with his dog. <br> <br> Training should be fun, not stressful. With patience and positive reinforcement, we help your dog build good habits and strengthen your bond. Whether it’s basic manners, leash etiquette, or tackling specific challenges, we’ll guide your pup step by step in a calm, supportive way.`,
      included: [
        "Positive reinforcement sessions",
        "Practice exercises",
        "Breaks for water & treats",
      ],
      durationOptions: "30 minutes / 60 minutes",
      price: "25.00€",
      images: [
        "/assets/img/FourthSection/img4.png",
        "/assets/img/FourthSection/img11.png",
        "/assets/img/FourthSection/img12.png",
      ],
    },
  },
  {
    src: "/assets/img/FourthSection/img5.png",
    title: "Pet Sitting (Dog & Cat – Owner’s House)",
    description:
      "Sometimes the best care is in the comfort of home. We’ll visit your pets where they feel safest, keeping their routine as normal as possible.",
    width: "md:w-[751px]",
    details: {
      title: "Pet Sitting (Dog & Cat)",
      description: `Sometimes the best care is in the comfort of home. We’ll visit your pets where they feel safest, keeping their routine as normal as possible. <br> <br> From feeding and play to cuddles and health check-ins, we give your pets all the love and attention they need while you’re away — so you return to happy paws and purrs.`,
      included: [
        "Feeding, water refresh",
        "Playtime & cuddles",
        "Litter cleaning or walks",
      ],
      durationOptions: "30 minutes / 60 minutes",
      price: "15.00€",
      images: [
        "/assets/img/FourthSection/img13.png",
        "/assets/img/FourthSection/img14.png",
        "/assets/img/FourthSection/img15.png",
      ],
    },
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