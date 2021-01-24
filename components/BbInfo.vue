<template>
  <v-card flat tile>
    <v-container fluid class="py-0">
      <v-row no-gutters justify="center">
        <v-row justify="center">
          <v-col cols="6" class="text-center text-h5">NEWS</v-col>
        </v-row>
        <v-col cols="12">
          <v-card-title class="justify-center red--text">
            当ジムにおける感染症対策について
          </v-card-title>
          <v-card-text>
            <v-row align="center" justify="center" class="pa-0">
              <p>
                新型コロナウイルスの感染が拡大しており、近畿にも緊急事態宣言が発出された状況を鑑みBB
                LABO.では日本フィットネス協会のガイドラインに沿って運営を行い、かつ自主的に営業を一部変更することといたしましたのでご報告させていただきます。
              </p>
            </v-row>
          </v-card-text>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class BbInfo extends Vue {}
</script>

<style lang="scss"></style>
