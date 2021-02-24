<template>
  <v-footer>
    <div class="d-flex flex-column">
    <div class="font-weight-bold">複合型トレーニングジム<br>BB LABO.</div>
    <div class="mt-4 font-weight-medium">兵庫県姫路市飾磨区<br>清水2-103</div>
      <div class="mt-4 font-weight-medium">完全予約制<br>駐車場2台あり</div>
    </div>
    <v-col class="text-center" cols="12">
      {{ new Date().getFullYear() }} — <strong>BB LABO.</strong>
    </v-col>
  </v-footer>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class MyFooter extends Vue {}
</script>

<style lang="scss" scoped></style>
