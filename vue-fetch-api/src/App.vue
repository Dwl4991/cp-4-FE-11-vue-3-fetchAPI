<script setup>
import { RouterView } from "vue-router";
import HomeView from "@/views/HomeView.vue";
</script>

<template>
  <!-- <RouterView /> -->
  <Suspense>
    <template #default>
      <HomeView />
    </template>
    <template #fallback>
      <div>Loading...</div>
    </template>
  </Suspense>
</template>

<style scoped></style>
