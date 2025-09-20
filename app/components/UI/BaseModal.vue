<template>
  <Transition name="modal">
    <div v-if="modelValue" class="modal-overlay" @click="closeOnOverlay">
      <div
        class="modal-container bg-[#54260A] rounded-[20px] px-3 md:px-10 py-6 w-full"
        :class="maxwidth"
        @click.stop
      >
        <div
          class="modal-body max-h-[70vh] w-full"
          :class="{ 'overflow-y-auto': overflowY }"
        >
          <slot></slot>
        </div>
      </div>
    </div>
  </Transition>
</template>

<script setup>
const props = defineProps({
  modelValue: {
    type: Boolean,
    required: true,
  },
  closeOnOutsideClick: {
    type: Boolean,
    default: true,
  },
  maxwidth: {
    type: String,
    default: "max-w-[1120px]",
  },
  overflowY: {
    type: Boolean,
    default: true,
  },
});

const emit = defineEmits(["update:modelValue", "close"]);

const close = () => {
  emit("update:modelValue", false);
  emit("close");
};

const closeOnOverlay = (e) => {
  if (props.closeOnOutsideClick) {
    close();
  }
};
</script>

