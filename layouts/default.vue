<template>
  <v-app>
    <v-container fluid pa-0>
      <bb-sub-nav v-if="$device.isDesktopOrTablet" />
      <v-main>
        <nuxt />
      </v-main>
      <v-footer>
        <span>&copy; {{ new Date().getFullYear() }}</span>
      </v-footer>
    </v-container>
  </v-app>
</template>
