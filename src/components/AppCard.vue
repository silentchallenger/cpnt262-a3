<script setup>
import AppButton from "./AppButton.vue";

defineProps({
  cardTitle: {
    type: String,
    default: "Default Card Title",
  },
  cardText: {
    type: String,
    default: "Default Card Text",
  },
});
</script>

<template>
  <section class="m-4 max-w-xs rounded-md bg-slate-200 p-4">
    <h3>{{ cardTitle }}</h3>
    <p>{{ cardText }}</p>
    <AppButton />
    <slot></slot>
  </section>
</template>
