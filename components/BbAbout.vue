<template>
  <v-card tile flat class="text-center">
    <div class="blue--text font-weight-bold text--darken-4 text-caption mt-6">
      ABOUT
    </div>
    <div class="text-h6 text-center font-weight-black">BB LABO.について</div>
    <div class="d-flex">
      <v-icon size="90">mdi-weight-lifter</v-icon>
      <v-card-text class="text-left">
        BB
        LABO.では初心者の方から経験者の方まで、全ての方ヘ最適なトレーニング方法を提案しています。
      </v-card-text>
      <v-btn class=""></v-btn>
    </div>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class BbAbout extends Vue {}
</script>

<style lang="scss"></style>
