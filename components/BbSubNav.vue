<template>
  <v-app-bar dense flat dark height="30px">
    <div class="bb-submenu-beginners-button">
      <a href="#">
        <v-icon color="white">mdi-chevron-right</v-icon>
        <span class="white--text font-weight-bold">初めての方へ</span>
      </a>
    </div>
    <div class="bb-submenu-book-button">
      <a href="#">
        <span class="white--text font-weight-bold">ご予約はこちら</span>
        <v-icon color="white" dense>mdi-book-minus-multiple-outline</v-icon>
      </a>
    </div>
  </v-app-bar>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class BbSubNav extends Vue {}
</script>

<style lang="scss">
.bb-submenu-beginners-button {
  align-self: center;
  a {
    margin: 0 auto;
    text-decoration: none;
  }
}

.bb-submenu-book-button {
  background-color: #f21d44;
  height: 100%;
  width: 15%;
  margin-left: auto;
  display: flex;
  align-items: center;
  a {
    margin: 0 auto;
    text-decoration: none;
  }
}
</style>
