<template>
  <div
    class="w-full border-2 border-[#F5F1E880] bg-[#F5F1E803] rounded-3xl sm:px-6 px-4 sm:py-6 py-4"
    style="backdrop-filter: blur(45px)"
  >
    <div class="w-full flex items-center gap-2 justify-between">
      <div class="flex items-center sm:-space-x-9 -space-x-5">
        <div class="sm:size-[60px] size-[40px] rounded-full bg-secondary">
          <img
            src="/assets/img/user1.png"
            alt="review-card-1"
            class="size-full object-cover"
          />
        </div>
        <div class="sm:size-[60px] size-[40px] rounded-full bg-secondary">
          <img
            src="/assets/img/user2.png"
            alt="review-card-2"
            class="size-full object-cover"
          />
        </div>
        <div class="sm:size-[60px] size-[40px] rounded-full bg-secondary">
          <img
            src="/assets/img/user3.png"
            alt="review-card-3"
            class="size-full object-cover"
          />
        </div>
        <div class="sm:size-[60px] size-[40px] rounded-full bg-secondary">
          <img
            src="/assets/img/user4.png"
            alt="review-card-4"
            class="size-full object-cover"
          />
        </div>
      </div>
      <div class="flex flex-col gap-0">
        <span
          class="text-secondary font-poppins sm:text-base text-sm font-medium"
          >5.0 rating — 1,500+ reviews</span
        >
        <div class="flex items-center gap-2">
          <div class="flex items-center gap-0">
            <svg
              v-for="i in 5"
              :key="i"
              width="17"
              height="16"
              viewBox="0 0 17 16"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M8.5 0L11.2479 4.71785L16.584 5.87336L12.9462 9.94465L13.4962 15.3766L8.5 13.175L3.50383 15.3766L4.05381 9.94465L0.416019 5.87336L5.7521 4.71785L8.5 0Z"
                fill="#D9C6AD"
              />
            </svg>
          </div>

          <span
            class="text-secondary font-poppins sm:text-base text-sm font-semibold"
            >Google Reviews</span
          >
        </div>
      </div>
    </div>
  </div>
</template>