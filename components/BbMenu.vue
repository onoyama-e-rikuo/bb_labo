<template>
  <v-col cols="12" sm="12" lg="6">
    <v-card outlined flat tile class="text-center pa-6">
      <div class="blue--text font-weight-bold text--darken-4 text-caption">
        料金について
      </div>
      <div class="text-h6 text-center font-weight-medium">PRICE</div>
      <v-icon size="90" class="mt-6">mdi-book-open</v-icon>
      <v-card-text>
        BB LABO.では初心者の方から経験者の方まで、<br />全ての方ヘ最適なトレーニング方法を提案しています。
      </v-card-text>
      <v-btn text nuxt to="/about" class="bb-menu-button">
        <span>
          もっと詳しく
          <v-icon small>mdi-arrow-right-thick</v-icon>
        </span>
      </v-btn>
    </v-card>
  </v-col>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class BbMenu extends Vue {}
</script>

<style lang="scss">
.bb-menu-button {
  .v-btn__content {
    border-top: 3px solid #364e8a;
    padding-top: 8px;
  }
}
</style>
