<template>
  <div class="box">
    <v-row no-gutters justify="center">
      <v-col cols="auto" align-self="center">
        <v-img contain :src="logoCube" height="100" width="100" />
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class BbFirstview extends Vue {
  private logoCube = require('../assets/images/bb_logo_cube_white.svg')
}
</script>

<style lang="scss">
.box {
  height: 100%;
  background-color: #364e8a;
  padding-top: 300px;
}
</style>
