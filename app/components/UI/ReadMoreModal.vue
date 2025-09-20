<template>
  <BaseModal v-model="open">
    <div class="w-full grid grid-cols-1 lg:grid-cols-10 gap-4 py-5">
      <div class="col-span-7 max-w-[705px]">
        <h2 class="text-primary font-poppins text-3xl font-semibold">
          {{ title }}
        </h2>
        <p
          class="text-septenary font-sf-pro-display text-xl font-normal pt-4"
          v-html="description"
        ></p>

        <div class="w-full grid grid-cols-1 md:grid-cols-3 gap-4 pt-10">
          <div
            class="rounded-lg bg-septenary/80 overflow-hidden w-[225px] h-[180px]"
            v-for="image in images"
            :key="image"
          >
            <img :src="image" alt="" class="w-full h-full object-cover" />
          </div>
        </div>
      </div>
      <div class="col-span-3 flex flex-col gap-4 justify-between">
        <div class="flex flex-col gap-8">
          <span class="text-primary font-semibold font-sf-pro-display text-lg">
            Included:
          </span>

          <div class="flex flex-col gap-2">
            <div
              class="flex items-center gap-2"
              v-for="included in included"
              :key="included"
            >
              <svg
                width="20"
                height="20"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7.49984 10.0003L9.1665 11.667L12.9165 7.91699M14.9175 4.16575C15.0891 4.58077 15.4185 4.91066 15.8332 5.08289L17.2875 5.68531C17.7026 5.85723 18.0323 6.18699 18.2042 6.60204C18.3762 7.0171 18.3762 7.48345 18.2042 7.8985L17.6023 9.35183C17.4303 9.76707 17.43 10.2339 17.6028 10.6489L18.2037 12.1018C18.289 12.3074 18.3328 12.5277 18.3329 12.7503C18.3329 12.9728 18.2891 13.1932 18.2039 13.3988C18.1188 13.6044 17.994 13.7912 17.8366 13.9485C17.6792 14.1059 17.4924 14.2306 17.2867 14.3157L15.8335 14.9177C15.4185 15.0893 15.0886 15.4187 14.9164 15.8335L14.314 17.2878C14.142 17.7029 13.8123 18.0327 13.3973 18.2046C12.9822 18.3765 12.5159 18.3765 12.1008 18.2046L10.6476 17.6026C10.2325 17.4311 9.76636 17.4314 9.35157 17.6036L7.89725 18.2051C7.48244 18.3766 7.01651 18.3765 6.60181 18.2047C6.18711 18.0329 5.85755 17.7036 5.68551 17.289L5.08294 15.8342C4.91134 15.4191 4.58196 15.0892 4.16721 14.917L2.71289 14.3146C2.29803 14.1427 1.96838 13.8132 1.79641 13.3984C1.62443 12.9836 1.62419 12.5174 1.79576 12.1024L2.39772 10.6491C2.56922 10.2341 2.56887 9.76787 2.39675 9.35306L1.79565 7.89765C1.71042 7.69208 1.66654 7.47172 1.6665 7.24919C1.66647 7.02665 1.71028 6.80628 1.79544 6.60069C1.8806 6.39509 2.00543 6.20829 2.16281 6.05095C2.32019 5.89362 2.50702 5.76884 2.71264 5.68375L4.16592 5.08176C4.58056 4.9103 4.91024 4.58133 5.08259 4.16704L5.68499 2.71267C5.8569 2.29761 6.18665 1.96785 6.60169 1.79593C7.01673 1.62401 7.48306 1.62401 7.8981 1.79593L9.35138 2.39792C9.76643 2.56942 10.2326 2.56907 10.6474 2.39695L12.1023 1.79687C12.5173 1.62504 12.9835 1.62508 13.3985 1.79696C13.8134 1.96885 14.1431 2.29852 14.3151 2.71346L14.9177 4.16827L14.9175 4.16575Z"
                  stroke="#AF4C0F"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>

              <span
                class="font-sf-pro-display text-base font-normal text-septenary"
                >{{ included }}</span
              >
            </div>
          </div>

          <div>
            <span
              class="text-primary font-semibold font-sf-pro-display text-lg"
            >
              Duration options
            </span>

            <p class="font-sf-pro-display text-lg font-normal text-septenary">
              {{ durationOptions }}
            </p>
          </div>

          <div>
            <span
              class="text-primary font-semibold font-sf-pro-display text-lg"
            >
              Price
            </span>

            <p class="font-sf-pro-display text-lg font-normal text-septenary">
              {{ price }}
            </p>
          </div>
        </div>

        <div class="flex items-center gap-2">
          <BaseButton
            class="text-lg font-semibold font-poppins border border-[#FFFFFF26]"
            >Acquire me</BaseButton
          >
          <BaseButton
            class="!bg-[#F5F1E80D] text-lg border-2 border-primary"
            style="backdrop-filter: blur(45px)"
            >Let’s talk</BaseButton
          >
        </div>
      </div>
    </div>
  </BaseModal>
</template>

<script setup>
import BaseModal from "@/components/UI/BaseModal.vue";
import BaseButton from "@/components/UI/BaseButton.vue";
const open = ref(false);

const title = ref("");
const description = ref("");
const images = ref([]);
const included = ref([]);
const durationOptions = ref("");
const price = ref("");

const openModal = (details) => {
  open.value = true;
  title.value = details.title;
  description.value = details.description;
  images.value = details.images;
  included.value = details.included;
  durationOptions.value = details.durationOptions;
  price.value = details.price;
};

defineExpose({
  openModal,
});
</script>