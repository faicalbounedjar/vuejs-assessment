<template>
  <v-app>
    <v-main>
      <Contact />
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import Contact from "./components/InfoContact.vue";
</script>
