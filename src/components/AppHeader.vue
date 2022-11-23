<script setup>
defineProps({
  title: {
    type: String,
    default: "Default Title",
  },
  context: {
    type: String,
    default: "Default Content",
  },
  color: {
    type: String,
    default: "text-indigo-500",
  },
});
</script>

<template>
  <header class="h-40 text-center">
    <h1
      class="py-4 text-3xl lg:text-4xl"
      :class="color"
    >
      {{ title }}
    </h1>
    <p class="text-xl">{{ context }}</p>
    <slot></slot>
  </header>
</template>
