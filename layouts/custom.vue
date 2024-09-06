<template>
  <v-layout class="rounded rounded-md" color="grey-darken-4">
    <v-app-bar color="surface-variant" title="C - Probigbike (Kawasaki Ninja H2®)"></v-app-bar>
    
    <v-navigation-drawer color="grey-darken-4">
      <v-list>
        <v-list-item title=" " ></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-navigation-drawer location="right" color="grey-darken-4">
      <v-list>
        <v-list-item title=" "></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main class="d-flex align-center justify-center" style="min-height: 300px; color: aqua;" >
      <NuxtPage />
      <!-- Main Content -->
    </v-main>
    
  </v-layout>
</template>
<script>
export default {
  data: () => ({
    items: Array.from({ length: 9 }, (k, v) => v + 1),
  }),
}
</script>