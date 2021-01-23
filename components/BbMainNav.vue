<template>
  <v-container fluid pa-0>
    <v-app-bar flat color="white">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>BB LABO.</v-toolbar-title>
      <v-spacer></v-spacer>
      <div class="text-center">
        <v-btn color="primary" large> 予約する </v-btn>
      </div>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list-item>
        <v-list-item-icon @click="drawer = !drawer">
          <v-icon>mdi-close</v-icon>
        </v-list-item-icon>
      </v-list-item>

      <div class="text-center my-6">
        <v-btn color="primary" width="80%" height="40"> 予約する </v-btn>
      </div>

      <v-divider></v-divider>

      <v-list class="mt-6">
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-container>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class BbMainNav extends Vue {
  private drawer: boolean = false

  private items = [
    { title: 'HOME', icon: 'mdi-home' },
    { title: 'ABOUT', icon: 'mdi-information' },
    { title: 'STAFF', icon: 'mdi-account-multiple' },
    { title: 'MENU', icon: 'mdi-book-open-page-variant' },
    { title: 'INTERVIEW', icon: 'mdi-forum' },
    { title: 'ACCESS', icon: 'mdi-google-maps' },
  ]
}
</script>

<style lang="scss"></style>
