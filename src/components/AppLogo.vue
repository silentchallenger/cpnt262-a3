<script setup>
defineProps({
  text: String,
  bgColor: {
    type: String,
    default: "bg-red-400",
  },
  src: String,
  alt: String,
});
</script>

<template>
  <button
    :class="bgColor"
    class="rounded-sd flex flex-col items-center justify-center p-4 text-black"
  >
    <img
      :src="src"
      :alt="alt"
      class="w-20"
    />{{ text }}
  </button>
</template>
