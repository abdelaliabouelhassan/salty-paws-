<template>
  <main class="w-full overflow-hidden relative">
    <Header />
    <slot />
    <Footer />
  </main>
</template>

<script setup>
import Header from "@/components/partials/Header.vue";
import Footer from "@/components/partials/Footer.vue";
</script>

<style scoped>
</style>