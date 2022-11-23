<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header class="flex items-center justify-between bg-slate-400 p-4 md:p-6">
    <div class="flex items-center gap-4">
      <p class="text-3xl font-bold text-slate-600">Project Site</p>
    </div>
    <nav>
      <ul class="flex gap-4">
        <li>
          <RouterLink
            to="/"
            class="text-xl font-bold text-slate-100"
            >Home</RouterLink
          >
        </li>
        <li>
          <RouterLink
            to="/about"
            class="text-xl font-bold text-slate-100"
            >About</RouterLink
          >
        </li>
      </ul>
    </nav>
  </header>

  <RouterView />
</template>
