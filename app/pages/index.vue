<template>
  <HeroSection />
</template>

<script setup>
import HeroSection from "@/components/partials/home/HeroSection.vue";
import { useHead } from "#app";

useHead({
  title: "Home",
});
</script>

<style scoped>
</style>