<script setup>
defineProps({
  text: Array,
});
</script>

<template>
  <ul class="flex flex-col items-center">
    <li
      v-for="(item, index) in text"
      :key="item.id"
    >
      {{ index + 1 }} - {{ item.text1 }} - {{ item.text2 }}
    </li>
  </ul>
</template>
