<script setup>
import AppHeader from "../components/AppHeader.vue";

const info = {
  title: "About Page",
  text: "This page is related to about page",
};
</script>

<template>
  <main>
    <AppHeader
      :title="info.title"
      :context="info.text"
    />
  </main>
</template>
