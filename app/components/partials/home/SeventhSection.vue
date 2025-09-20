<template>
  <section class="py-10 md:pb-40" id="faqs">
    <div class="text-center">
      <h2
        class="text-septenary font-sf-pro-display font-semibold text-4xl mb-14"
      >
        Your questions, answered
      </h2>
    </div>
    <div class="w-full max-w-[1095px] mx-auto px-4">
      <div class="flex flex-col lg:flex-row gap-8 lg:gap-12">
        <!-- Left Column - Navigation -->
        <div class="lg:w-1/3">
          <div class="flex flex-col gap-2">
            <button
              v-for="category in categories"
              :key="category.id"
              @click="setActiveCategory(category.id)"
              :class="[
                'flex items-center gap-3 px-4 py-3 rounded-xl cursor-pointer h-[60px] text-left transition-all duration-200',
                activeCategory === category.id
                  ? 'bg-primary text-secondary'
                  : 'bg-septenary/3 text-septenary hover:text-secondary hover:bg-primary',
              ]"
            >
              <svg
                v-if="activeCategory === category.id"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="2"
                stroke="currentColor"
                class="w-4 h-4"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M8.25 4.5l7.5 7.5-7.5 7.5"
                />
              </svg>
              <span class="font-medium">{{ category.name }}</span>
            </button>
          </div>
        </div>

        <!-- Right Column - FAQ Content -->
        <div class="lg:w-2/3">
          <Transition
            enter-active-class="transition-all duration-300 ease-out"
            enter-from-class="opacity-0 translate-y-4"
            enter-to-class="opacity-100 translate-y-0"
            leave-active-class="transition-all duration-200 ease-in"
            leave-from-class="opacity-100 translate-y-0"
            leave-to-class="opacity-0 -translate-y-4"
            mode="out-in"
          >
            <div key="faq-content" class="space-y-4">
              <div
                v-for="(faq, index) in activeFaqs"
                :key="`${activeCategory}-${index}`"
                class="border-b border-septenary/15 pb-4"
              >
                <button
                  @click="toggleFaq(index)"
                  class="w-full flex items-center justify-between text-left py-2 cursor-pointer"
                >
                  <h3
                    class="text-septenary font-semibold text-xl font-poppins pr-4"
                  >
                    {{ faq.question }}
                  </h3>
                  <div class="flex-shrink-0">
                    <Transition
                      enter-active-class="transition-all duration-200 ease-out"
                      enter-from-class="opacity-0 rotate-90"
                      enter-to-class="opacity-100 rotate-0"
                      leave-active-class="transition-all duration-200 ease-in"
                      leave-from-class="opacity-100 rotate-0"
                      leave-to-class="opacity-0 rotate-90"
                      mode="out-in"
                    >
                      <svg
                        v-if="expandedFaqs.includes(index)"
                        key="minus"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="2"
                        stroke="currentColor"
                        class="w-5 h-5 text-primary"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          d="M5 12h14"
                        />
                      </svg>
                      <svg
                        v-else
                        key="plus"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="2"
                        stroke="currentColor"
                        class="w-5 h-5 text-primary"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          d="M12 4.5v15m7.5-7.5h-15"
                        />
                      </svg>
                    </Transition>
                  </div>
                </button>

                <Transition
                  enter-active-class="transition-all duration-300 ease-out"
                  enter-from-class="opacity-0 max-h-0"
                  enter-to-class="opacity-100 max-h-96"
                  leave-active-class="transition-all duration-300 ease-in"
                  leave-from-class="opacity-100 max-h-96"
                  leave-to-class="opacity-0 max-h-0"
                >
                  <div
                    v-if="expandedFaqs.includes(index)"
                    class="mt-3 text-septenary leading-relaxed text-lg font-sf-pro-display overflow-hidden"
                  >
                    {{ faq.answer }}
                  </div>
                </Transition>
              </div>
            </div>
          </Transition>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from "vue";

const activeCategory = ref("general");
const expandedFaqs = ref([0]); // First FAQ expanded by default

const categories = [
  { id: "general", name: "General" },
  { id: "services", name: "Services" },
  { id: "location", name: "Location & Availability" },
  { id: "pricing", name: "Pricing & Conditions" },
  { id: "requirements", name: "Pet Requirements" },
];

const faqData = {
  general: [
    {
      question: "What kind of pets do you care for?",
      answer:
        "We specialize in caring for dogs and cats of all breeds, sizes, and ages. Our experienced team is trained to handle various temperaments and special needs, ensuring every pet receives personalized attention and care.",
    },
    {
      question: "Do you have pet care training or experience?",
      answer:
        "Yes, our team consists of certified pet care professionals with extensive experience in animal behavior, first aid, and specialized care techniques. We regularly update our training to stay current with best practices in pet care.",
    },
    {
      question: "Do you offer services in English and Portuguese?",
      answer:
        "Absolutely! We provide all our services in both English and Portuguese, ensuring clear communication with pet owners and seamless care for your beloved companions.",
    },
  ],
  services: [
    {
      question: "What services do you offer?",
      answer:
        "We offer comprehensive pet care services including dog daycare, boarding, walking, training, and in-home pet sitting for both dogs and cats. Each service is tailored to meet your pet's specific needs.",
    },
    {
      question: "Do you provide overnight pet sitting?",
      answer:
        "Yes, we offer overnight pet sitting services where our caregivers stay in your home to provide 24/7 care and companionship for your pets while you're away.",
    },
    {
      question: "Can you administer medication to pets?",
      answer:
        "Our trained professionals can administer oral medications and basic medical care as prescribed by your veterinarian. We maintain detailed records of all medical care provided.",
    },
  ],
  location: [
    {
      question: "What areas do you serve?",
      answer:
        "We currently serve the greater metropolitan area and surrounding suburbs. Please contact us to confirm if we provide services in your specific location.",
    },
    {
      question: "Do you offer services on weekends and holidays?",
      answer:
        "Yes, we provide services seven days a week, including weekends and most holidays. Holiday rates may apply for certain dates.",
    },
    {
      question: "How far in advance should I book?",
      answer:
        "We recommend booking at least one week in advance, especially for holiday periods and extended stays. However, we do our best to accommodate last-minute requests when possible.",
    },
  ],
  pricing: [
    {
      question: "How do you determine pricing?",
      answer:
        "Pricing is based on the type of service, duration, number of pets, and any special requirements. We offer competitive rates and transparent pricing with no hidden fees.",
    },
    {
      question: "Do you offer discounts for multiple pets?",
      answer:
        "Yes, we offer discounts for families with multiple pets. The discount varies based on the number of pets and services requested.",
    },
    {
      question: "What payment methods do you accept?",
      answer:
        "We accept cash, credit cards, bank transfers, and digital payment methods. Payment is typically due at the time of service or as arranged in advance.",
    },
  ],
  requirements: [
    {
      question: "What vaccinations are required?",
      answer:
        "All pets must be up-to-date on core vaccinations including rabies, DHPP (for dogs), and FVRCP (for cats). We may also require additional vaccinations based on the service type.",
    },
    {
      question: "Do you accept aggressive pets?",
      answer:
        "We work with pets of various temperaments, but we require a consultation for pets with known aggression issues to ensure the safety of all animals and our staff.",
    },
    {
      question: "What if my pet has special dietary needs?",
      answer:
        "We're happy to accommodate special dietary requirements, medications, and feeding schedules. Please provide detailed instructions and any necessary supplies.",
    },
  ],
};

const activeFaqs = computed(() => {
  return faqData[activeCategory.value] || [];
});

const toggleFaq = (index) => {
  const expandedIndex = expandedFaqs.value.indexOf(index);
  if (expandedIndex > -1) {
    expandedFaqs.value.splice(expandedIndex, 1);
  } else {
    expandedFaqs.value.push(index);
  }
};

// Reset expanded FAQs when category changes
const setActiveCategory = (categoryId) => {
  activeCategory.value = categoryId;
  expandedFaqs.value = [0]; // Reset to first FAQ expanded
};
</script>

<style scoped>
</style>
