<template>
  <div>
    <div class="d-flex">
      <div class="text-h4 font-weight-medium mr-4">
        <div>西川</div>
        <div class="text-caption font-weight-medium">Nishikawa</div>
      </div>
      <div class="text-h4 font-weight-medium">
        <div>雅人</div>
        <div class="text-caption font-weight-medium">Masato</div>
      </div>
    </div>
    <v-img :src="trainer1" class="mt-8"></v-img>
    <div class="text-h5 font-weight-medium mt-8">西川 雅人</div>
    <div class="text-caption font-weight-medium">代表/パーソナルトレーナー</div>
    <div class="text-body-1 font-weight-medium mt-8">経歴</div>
    <p class="text-body-2 mt-4">
      個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。
    </p>
    <div class="text-body-1 font-weight-medium mt-8">メッセージ</div>
    <p class="text-body-2 mt-4">
      簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。
    </p>
    <div class="d-flex mt-16">
      <div class="text-h4 font-weight-medium mr-4">
        <div>師</div>
        <div class="text-caption font-weight-medium">Shi</div>
      </div>
      <div class="text-h4 font-weight-medium">
        <div>匠</div>
        <div class="text-caption font-weight-medium">Shou</div>
      </div>
    </div>
    <v-img :src="trainer2" class="mt-8"></v-img>
    <div class="text-h5 font-weight-medium mt-8">師匠</div>
    <div class="text-caption font-weight-medium">整体師</div>
    <div class="text-body-1 font-weight-medium mt-8">経歴</div>
    <p class="text-body-2 mt-4">
      個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。個人の簡単な経歴をここに書く。
    </p>
    <div class="text-body-1 font-weight-medium mt-8">メッセージ</div>
    <p class="text-body-2 mt-4 mb-16">
      簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。簡単に思いやビジョンを書く。
    </p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class Trainer extends Vue {
  private trainer1 = require('../assets/images/trainer1.jpeg')
  private trainer2 = require('../assets/images/trainer2.jpeg')
}
</script>

<style lang="scss" scoped>
.number {
  border-bottom: solid 4px black;
}
</style>
