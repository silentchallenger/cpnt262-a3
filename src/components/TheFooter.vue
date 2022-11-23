<script setup>
// Set v-bind for later use if needed
defineProps({
  copyright: {
    type: String,
    default: "Copyright 2022 Test Project. All rights reserved.",
  },
});

const copyright = "Copyright 2022 Vue Project. All rights reserved.";
</script>

<template>
  <footer class="flex h-20 items-center bg-slate-300">
    <p class="m-auto text-xl">{{ copyright }}</p>
  </footer>
</template>
