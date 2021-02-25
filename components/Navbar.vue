<template>
  <div>
    <v-app-bar flat fixed elevate-on-scroll>
      <v-icon class="navbar-menu-icon" @click="drawer = !drawer"
        >mdi-menu</v-icon
      >
      <h2 class="navbar-title">BB LABO.</h2>
      <v-btn width="25%" small outlined tile class="navbar-reservation-button"
        >Web予約</v-btn
      >
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app>
      <v-list-item>
        <v-list-item-icon @click="drawer = !drawer">
          <v-icon>mdi-close</v-icon>
        </v-list-item-icon>
      </v-list-item>

      <v-divider></v-divider>

      <v-list class="mt-6">
        <v-list-item v-for="item in items" :key="item.title" :to="item.path">
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
export default class Navbar extends Vue {
  private drawer: boolean = false

  private items = [
    { title: 'Home', icon: 'mdi-home', path: '/' },
    { title: 'Programs', icon: 'mdi-dumbbell', path: '/programs' },
    { title: 'Trainers', icon: 'mdi-account-multiple', path: '/trainers' },
    { title: 'Interview', icon: 'mdi-forum', path: '/interview' },
    { title: 'Location', icon: 'mdi-google-maps', path: '/location' },
  ]

  private logoTextWhite = require('../assets/images/bb_logo_text_white.svg')
  private logoText = require('../assets/images/bb_logo_text.svg')

  private scrollY = 0

  private windowHeight = 0

  private isClient = process.client

  created() {
    if (this.isClient) {
      window.addEventListener('scroll', this.handleScroll)
      this.handleScroll()
      window.addEventListener('resize', this.handleResize)
      this.handleResize()
    }
  }

  destroyed() {
    if (this.isClient) {
      window.addEventListener('scroll', this.handleScroll)
    }
  }

  private handleScroll() {
    if (this.isClient) {
      this.scrollY = window.scrollY
    }
  }

  handleResize() {
    this.windowHeight = window.innerHeight
  }

  private isInsideOfFirstview() {
    if (this.scrollY < this.windowHeight - 30) {
      return true
    }
  }
}
</script>

<style lang="scss" scoped>
::v-deep .v-toolbar__content {
  width: 100%;
  position: relative;
  display: flex;
}
.navbar-menu-icon {
  position: absolute;
}
.navbar-title {
  margin: 0 auto;
}
.navbar-reservation-button {
  background-color: white;
  position: absolute;
  right: 16px;
}
</style>
