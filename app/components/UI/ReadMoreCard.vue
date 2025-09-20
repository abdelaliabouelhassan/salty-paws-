<template>
  <div class="w-full h-full group">
    <div
      class="w-full h-[452px] bg-septenary/80 rounded-[20px] overflow-hidden relative"
    >
      <img
        :src="src"
        alt=""
        class="w-full h-full object-cover group-hover:opacity-60 transition-all duration-200"
      />
      <div
        class="absolute hidden group-hover:flex duration-200 top-0 left-0 w-full h-full justify-center items-center p-4"
      >
        <BaseButton
          @click="openModal()"
          class="text-lg font-semibold font-poppins text-secondary border border-[#FFFFFF26]"
          style="backdrop-filter: blur(4px)"
          >See more</BaseButton
        >
      </div>
    </div>
    <div class="flex flex-col gap-2 w-full py-4">
      <h4 class="text-primary font-poppins text-base sm:text-2xl font-semibold">
        {{ title }}
      </h4>
      <p
        class="text-septenary font-sf-pro-display font-normal text-lg sm:text-xl text-start max-w-[607px]"
      >
        {{ description }}
      </p>
    </div>
  </div>
</template>

<script setup>
import BaseButton from "@/components/UI/BaseButton.vue";
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  src: {
    type: String,
    required: true,
  },
  openModal: {
    type: Function,
    required: true,
  },
});
</script>


<style scoped>
</style>