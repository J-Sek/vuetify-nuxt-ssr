<template>
  <v-app>
    <AppSidebar v-model="drawer" />

    <AppHeader @toggle:sidebar="drawer = !drawer" />

    <v-main>
      <nuxt-page />
    </v-main>

    <v-btn
      class="ma-2"
      icon="mdi-theme-light-dark"
      location="bottom right"
      position="absolute"
      @click="$vuetify.theme.cycle()"
    />
  </v-app>
</template>

<script lang="ts" setup>
  const drawer = ref(true)
</script>
