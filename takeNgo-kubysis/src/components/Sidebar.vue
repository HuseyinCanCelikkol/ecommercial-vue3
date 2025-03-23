<template>
    <v-app>
      <v-navigation-drawer v-model="drawer" app>
        <v-list dense>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-view-dashboard</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Dashboard</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
  
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-account-group</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Users</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
  
          <v-list-group prepend-icon="mdi-folder">
            <template #activator>
              <v-list-item-title>Management</v-list-item-title>
            </template>
  
            <v-list-item link>
              <v-list-item-icon>
                <v-icon>mdi-file-document</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>Reports</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
  
            <v-list-item link>
              <v-list-item-icon>
                <v-icon>mdi-cog</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>Settings</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </v-list>
      </v-navigation-drawer>
  
      <v-app-bar app>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title>My App</v-toolbar-title>
      </v-app-bar>
  
      <v-main>
        <router-view></router-view>
      </v-main>
    </v-app>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const drawer = ref(true);
  </script>
  
  <style scoped>
  .v-navigation-drawer {
    background-color: #ffffff;
  }
  </style>
  