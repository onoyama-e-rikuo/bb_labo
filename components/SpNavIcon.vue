<template>
  <div>
    <v-img
      v-if="isInsideOfFirstview()"
      contain
      :src="logoTextWhite"
      width="150"
      class="bb-nav-logo-text"
    />
    <v-img
      v-else
      contain
      :src="logoText"
      width="150"
      class="bb-nav-logo-text"
    />
    <v-btn
      fab
      height="45"
      width="45"
      @click.stop="drawer = !drawer"
      class="bb-nav-icon"
    >
      <v-icon size="30" color="white">mdi-menu</v-icon>
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

<style lang="scss">
.bb-nav-logo-text {
  position: fixed;
  top: 30px;
  left: 10px;
  z-index: 1;
}

.bb-nav-icon {
  position: fixed;
  top: 20px;
  right: 10px;
  z-index: 1;
}

.v-btn--is-elevated.v-btn--fab {
  box-shadow: none;
}

.theme--light.v-btn.v-btn--has-bg {
  background-color: gray;
}
</style>
