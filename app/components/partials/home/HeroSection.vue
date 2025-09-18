<template>
  <div>
    <div class="w-full h-screen xl:h-[1080px] relative">
      <img
        src="/assets/img/hero.webp"
        alt="hero-section"
        class="w-full h-full object-cover"
      />
      <div
        class="absolute top-0 left-0 right-0 bottom-0 hero-section-gradient"
      ></div>
    </div>
  </div>
</template>

<script setup>
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