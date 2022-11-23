<script setup>
defineProps({
  text: {
    type: String,
    default: "Click me!",
  },
  bgColor: {
    type: String,
    default: "bg-red-300",
  },
});
</script>

<template>
  <button
    :class="bgColor"
    class="rounded-sd flex flex-col items-center justify-center p-2 text-black"
  >
    {{ text }}
  </button>
</template>
