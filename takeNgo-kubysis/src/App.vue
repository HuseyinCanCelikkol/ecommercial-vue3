<template>
  <v-app>
    <Sidebar />

    <v-app-bar app>
      <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
      <v-toolbar-title>My App</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script setup>
import Sidebar from './components/Sidebar.vue';
import { ref } from 'vue';

const drawer = ref(true);
const toggleDrawer = () => {
  drawer.value = !drawer.value;
};
</script>
