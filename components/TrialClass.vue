<template>
  <div>
    <div>
      <div class="text-h5 font-weight-medium mt-8">Trial Class</div>
      <p class="text-body-2 mt-8">
        トライアルクラスの説明。トライアルクラスの説明。トライアルクラスの説明。トライアルクラスの説明。トライアルクラスの説明。トライアルクラスの説明。
      </p>
      <div class="mock mt-8"></div>
    </div>
    <div class="text-center">
      <div class="mt-16">
        <span class="number text-h4 font-weight-medium">01</span>
        <div class="text-h6 font-weight-bold mt-4">カウンセリング</div>
        <p class="text-body-2 mt-6 px-6">
          トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。
        </p>
      </div>
      <div class="mt-16">
        <span class="number text-h4 font-weight-medium">02</span>
        <div class="text-h6 font-weight-bold mt-4">ウォームアップ</div>
        <p class="text-body-2 mt-6 px-6">
          トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。
        </p>
      </div>
      <div class="mt-16">
        <span class="number text-h4 font-weight-medium">03</span>
        <div class="text-h6 font-weight-bold mt-4">マシントレーニング</div>
        <p class="text-body-2 mt-6 px-6">
          トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。
        </p>
      </div>
      <div class="mt-16">
        <span class="number text-h4 font-weight-medium">04</span>
        <div class="text-h6 font-weight-bold mt-4">クールダウン</div>
        <p class="text-body-2 mt-6 px-6">
          トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。
        </p>
      </div>
      <div class="mt-16">
        <span class="number text-h4 font-weight-medium">05</span>
        <div class="text-h6 font-weight-bold mt-4">フィードバック</div>
        <p class="text-body-2 mt-6 px-6">
          トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。トレーニングの説明。
        </p>
      </div>
    </div>
    <v-divider class="mt-16"></v-divider>
    <div class="text-center">
      <div class="text-h4 font-weight-medium mt-12">Schedule</div>
      <div class="text-subtitle-2">ご予約は予約専用サイトから受け付けております<br>お気軽にご連絡ください</div>
      <v-btn width="60%" x-large outlined tile class="mt-8 font-weight-bold">Web予約はこちら</v-btn>
      <div class="mt-8 text-caption">※ご予約のキャンセルは事前にお電話にて<br>ご連絡お願いいたします</div>
      <div class="mt-4 text-caption">キャンセル専用電話番号</div>
      <div class="text-subtitle-1">080 5964 5422</div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class TrialClass extends Vue {}
</script>

<style lang="scss" scoped>
.mock {
  background-color: darkgray;
  height: 400px;
}

.number {
  border-bottom: solid 4px black;
}
</style>
