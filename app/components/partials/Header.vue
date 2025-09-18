<template>
  <header class="w-full absolute top-0 left-0 right-0 z-10">
    <div
      class="max-w-[1461px] mx-auto py-4 px-4 flex justify-between items-center"
    >
      <NuxtLink
        to="/"
        class="flex items-center gap-2 text-secondary font-poppins text-xl font-semibold"
      >
        <img src="/assets/icons/logo.svg" alt="logo" class="size-8" />
        Salty Paws
      </NuxtLink>

      <!-- Desktop Navigation -->
      <div class="hidden lg:flex items-center gap-8">
        <div class="flex items-center gap-4">
          <NuxtLink
            v-for="link in navLinks"
            :key="link.to"
            :to="link.to"
            class="flex items-center gap-2 text-secondary font-sf-pro-display text-base font-medium hover:opacity-80 transition-opacity"
          >
            {{ link.label }}
          </NuxtLink>
        </div>
        <svg
          width="1"
          height="14"
          viewBox="0 0 1 14"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <line
            opacity="0.25"
            x1="0.5"
            y1="-2.18557e-08"
            x2="0.500001"
            y2="14"
            stroke="#F5F1E8"
          />
        </svg>

        <div class="flex items-center gap-4">
          <button
            class="text-secondary font-sf-pro-display text-base font-medium cursor-pointer hover:opacity-80 transition-opacity"
          >
            Contact
          </button>
          <BaseButton class="text-base font-medium font-sf-pro-display"
            >Acquire us</BaseButton
          >
        </div>
      </div>

      <!-- Mobile Menu Button -->
      <button
        @click="toggleMobileMenu"
        class="lg:hidden flex flex-col gap-1 p-2"
        aria-label="Toggle menu"
      >
        <span
          class="w-6 h-0.5 bg-secondary transition-all duration-300"
          :class="{ 'rotate-45 translate-y-2': isMobileMenuOpen }"
        ></span>
        <span
          class="w-6 h-0.5 bg-secondary transition-all duration-300"
          :class="{ 'opacity-0': isMobileMenuOpen }"
        ></span>
        <span
          class="w-6 h-0.5 bg-secondary transition-all duration-300"
          :class="{ '-rotate-45 -translate-y-2': isMobileMenuOpen }"
        ></span>
      </button>
    </div>

    <!-- Mobile Menu Overlay -->
    <Transition
      enter-active-class="transition-all duration-300 ease-out"
      enter-from-class="opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="transition-all duration-300 ease-in"
      leave-from-class="opacity-100"
      leave-to-class="opacity-0"
    >
      <div
        v-if="isMobileMenuOpen"
        class="fixed inset-0 bg-black/50 bg-opacity-50 z-40"
        @click="closeMobileMenu"
      ></div>
    </Transition>

    <!-- Mobile Menu -->
    <Transition
      enter-active-class="transition-all duration-300 ease-out"
      enter-from-class="transform translate-x-full"
      enter-to-class="transform translate-x-0"
      leave-active-class="transition-all duration-300 ease-in"
      leave-from-class="transform translate-x-0"
      leave-to-class="transform translate-x-full"
    >
      <div
        v-if="isMobileMenuOpen"
        class="fixed top-0 right-0 h-full w-80 max-w-[90vw] bg-white shadow-xl z-50 lg:hidden"
      >
        <!-- Mobile Menu Header -->
        <div
          class="flex justify-between items-center p-6 border-b border-gray-100"
        >
          <div
            class="flex items-center gap-2 text-gray-800 font-poppins text-xl font-semibold"
          >
            <img src="/assets/icons/logo.svg" alt="logo" class="size-8" />
            Salty Paws
          </div>
          <button
            @click="closeMobileMenu"
            class="p-2 hover:bg-gray-100 rounded-full transition-colors"
            aria-label="Close menu"
          >
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M18 6L6 18M6 6L18 18"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </button>
        </div>

        <!-- Mobile Menu Content -->
        <div class="flex flex-col p-6 space-y-6">
          <!-- Navigation Links -->
          <nav class="space-y-4">
            <NuxtLink
              v-for="link in navLinks"
              :key="link.to"
              :to="link.to"
              @click="closeMobileMenu"
              class="block text-gray-800 font-sf-pro-display text-lg font-medium py-2 hover:text-blue-600 transition-colors border-b border-gray-100 last:border-b-0"
            >
              {{ link.label }}
            </NuxtLink>
          </nav>

          <!-- Action Buttons -->
          <div class="space-y-4 pt-4">
            <button
              @click="closeMobileMenu"
              class="w-full text-left text-gray-800 font-sf-pro-display text-lg font-medium py-3 hover:text-blue-600 transition-colors"
            >
              Contact
            </button>
            <BaseButton
              class="w-full justify-center font-sf-pro-display text-base font-medium"
              @click="closeMobileMenu"
            >
              Acquire us
            </BaseButton>
          </div>
        </div>
      </div>
    </Transition>
  </header>
</template>

<script setup>
import { ref } from "vue";
import BaseButton from "@/components/UI/BaseButton.vue";

const navLinks = [
  {
    to: "/#about",
    label: "About",
  },
  {
    to: "/#services",
    label: "Services",
  },
  {
    to: "/#coverage-area",
    label: "Coverage area",
  },
  {
    to: "/#faqs",
    label: "FAQs",
  },
];

const isMobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false;
};

// Close mobile menu when route changes (optional)
const router = useRouter?.();
if (router) {
  router.afterEach(() => {
    closeMobileMenu();
  });
}

// Close mobile menu on escape key
const handleKeydown = (event) => {
  if (event.key === "Escape" && isMobileMenuOpen.value) {
    closeMobileMenu();
  }
};

onMounted(() => {
  document.addEventListener("keydown", handleKeydown);
});

onUnmounted(() => {
  document.removeEventListener("keydown", handleKeydown);
});
</script>

<style scoped>
/* Additional styles if needed */
</style>