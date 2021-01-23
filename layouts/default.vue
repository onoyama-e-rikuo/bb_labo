<template>
  <v-app>
    <v-container fluid pa-0>
      <bb-sub-nav v-if="$device.isDesktopOrTablet" />
      <bb-main-nav />
      <v-main>
        <nuxt />
      </v-main>
    </v-container>
  </v-app>
</template>
