<template>
  <div>
    <v-btn
      fab
      height="50"
      width="50"
      @click.stop="drawer = !drawer"
      color="primary"
      class="bb-nav-icon"
    >
      <v-icon size="30">mdi-menu</v-icon>
    </v-btn>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      right
      style="z-index: 2"
    >
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
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class SpNavIcon extends Vue {
  private drawer: boolean = false

  private items = [
    { title: 'HOME', icon: 'mdi-home' },
    { title: 'ABOUT', icon: 'mdi-information' },
    { title: 'STAFF', icon: 'mdi-account-multiple' },
    { title: 'PRICE', icon: 'mdi-book-open-page-variant' },
    { title: 'INTERVIEW', icon: 'mdi-forum' },
    { title: 'ACCESS', icon: 'mdi-google-maps' },
  ]
}
</script>

<style lang="scss">
.bb-nav-icon {
  position: fixed;
  top: 40px;
  right: 30px;
  z-index: 1;
}

.v-btn--is-elevated.v-btn--fab {
  box-shadow: none;
}
</style>
