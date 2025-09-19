<template>
  <HeroSection />
  <FirstSection />
  <SecondSection />
  <ThirdSection />
  <FourthSection />
  <FifthSection />
</template>

<script setup>
import HeroSection from "@/components/partials/home/HeroSection.vue";
import FirstSection from "@/components/partials/home/FirstSection.vue";
import SecondSection from "@/components/partials/home/SecondSection.vue";
import ThirdSection from "@/components/partials/home/ThirdSection.vue";
import FourthSection from "@/components/partials/home/FourthSection.vue";
import FifthSection from "@/components/partials/home/FifthSection.vue";
import { useHead } from "#app";

useHead({
  title: "Home",
});
</script>

<style scoped>
</style>