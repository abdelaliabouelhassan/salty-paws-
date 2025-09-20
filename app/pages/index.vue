<template>
  <HeroSection />
  <FirstSection />
  <div class="py-14">
    <LoopLine />
  </div>
  <SecondSection />
  <ThirdSection />
  <FourthSection />
  <FifthSection />
  <SixthSection />
  <SeventhSection />
  <EightSection />
</template>

<script setup>
import HeroSection from "@/components/partials/home/HeroSection.vue";
import FirstSection from "@/components/partials/home/FirstSection.vue";
import SecondSection from "@/components/partials/home/SecondSection.vue";
import ThirdSection from "@/components/partials/home/ThirdSection.vue";
import FourthSection from "@/components/partials/home/FourthSection.vue";
import FifthSection from "@/components/partials/home/FifthSection.vue";
import SixthSection from "@/components/partials/home/SixthSection.vue";
import SeventhSection from "@/components/partials/home/SeventhSection.vue";
import EightSection from "@/components/partials/home/EightSection.vue";
import LoopLine from "@/components/UI/LoopLine.vue";
import { useHead } from "#app";

useHead({
  title: "Home",
});
</script>

<style scoped>
</style>