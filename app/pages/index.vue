<template>
  <HeroSection />
  <FirstSection />
  <SecondSection />
</template>

<script setup>
import HeroSection from "@/components/partials/home/HeroSection.vue";
import FirstSection from "@/components/partials/home/FirstSection.vue";
import SecondSection from "@/components/partials/home/SecondSection.vue";
import { useHead } from "#app";

useHead({
  title: "Home",
});
</script>

<style scoped>
</style>