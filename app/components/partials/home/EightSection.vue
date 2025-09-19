<template>
  <section class="w-full relative">
    <div>
      <img
        src="/assets/img/EightSection/img1.webp"
        class="w-full h-[550px] object-cover"
        alt=""
      />
    </div>

    <div class="absolute top-0 left-0 w-full h-full">
      <div
        class="max-w-[1320px] px-4 mx-auto flex flex-col justify-center h-full"
      >
        <p
          class="text-secondary font-poppins font-semibold md:text-4xl text-2xl max-w-[709px]"
        >
          Let’s talk and book the most caring, fun, fresh and cuddling daycare
          for your family member ❤️
        </p>

        <div class="flex items-center gap-4 pt-10">
          <BaseButton
            class="bg-secondary text-septenary font-poppins font-semibold md:text-lg text-base"
          >
            Acquire me
          </BaseButton>
          <BaseButton
            class="text-secondary bg-transparent border-2 border-secondary font-poppins font-semibold text-lg"
            style="backdrop-filter: blur(45px)"
          >
            Let’s talk</BaseButton
          >
        </div>
      </div>
    </div>
  </section>
</template>


<script setup>
import BaseButton from "@/components/UI/BaseButton.vue";
</script>