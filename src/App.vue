<template>
  <SiteHeader />
  <main class="page">
    <div class="wrapper">
      <RouterView />
    </div>
  </main>
</template>

<script setup>
import SiteHeader from './components/SiteHeader.vue'
import { RouterView } from 'vue-router'
</script>
