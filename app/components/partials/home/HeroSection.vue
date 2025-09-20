<template>
  <div class="w-full">
    <div class="w-full h-screen xl:h-[1080px] relative">
      <img
        src="/assets/img/hero.webp"
        alt="hero-section"
        class="w-full h-full object-cover"
      />
      <div
        class="absolute top-0 left-0 right-0 bottom-0 hero-section-gradient"
      ></div>

      <div class="absolute top-0 left-0 w-full h-full">
        <div class="max-w-[1500px] h-full mx-auto flex px-4">
          <div class="my-auto max-w-[591px] flex flex-col gap-6">
            <h1
              class="text-secondary font-poppins md:text-[54px] md:leading-[72px] text-4xl font-semibold"
            >
              Happy paws, <br />
              wagging tails, and <br />
              fresh air every day.
            </h1>
            <p
              class="text-[#F5F1E8] font-sf-pro-display md:text-xl text-base font-normal"
            >
              We treat every dog like part of our family, creating a safe,
              caring, and stimulating environment that supports both their
              physical health and emotional well-being.
            </p>

            <div class="flex items-center gap-4">
              <BaseButton
                class="text-lg font-semibold font-poppins border border-[#FFFFFF26]"
                >Contact</BaseButton
              >
              <BaseButton
                class="!bg-[#F5F1E80D] border-2 text-lg border-secondary"
                style="backdrop-filter: blur(45px)"
                >Let’s talk</BaseButton
              >
            </div>

            <div class="w-full max-w-[415px] pt-10">
              <ReviewCard />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import BaseButton from "@/components/UI/BaseButton.vue";
import ReviewCard from "@/components/UI/ReviewCard.vue";
</script>

<style scoped>
.hero-section-gradient {
  background: linear-gradient(
    274.02deg,
    rgba(84, 84, 84, 0) 6.71%,
    #545454 70.59%
  );
  opacity: 0.75;
}
</style>