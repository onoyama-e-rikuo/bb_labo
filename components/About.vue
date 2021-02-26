<template>
  <div class="pa-6">
    <div class="text-center mt-10">
      <v-dialog scrollable v-model="dialog">
        <template v-slot:activator="{ on, attrs }">
          <v-btn outlined tile v-bind="attrs" v-on="on" class="font-weight-bold"
            >当ジムにおける感染症対策について</v-btn
          >
        </template>

        <v-card height="600">
          <v-card-title> 新型コロナウイルス対策について </v-card-title>
          <v-divider></v-divider>
          <v-card-text class="mt-4">
            日頃よりスポーツクラブメガロスをご愛顧いただき、誠にありがとうございます。
            ご利用される皆様がより安心して施設をご利用いただくため、施設のご利用に関しては「密集」「密接」「密閉」の３つの「密」が重ならないように注意を払うとともに、手洗い・うがいの徹底やマスク（ネックゲイターを含む）の着用のほか、フィジカルディスタンス（身体的距離の確保）に配慮した対策を進めていきます。
            お客様におかれましては、ご自身の健康管理にご留意いただき、しばらくの間、館内掲示やホームページに記載の症状がある方や該当する点がある方、基礎疾患がある方は極力ご利用をお控えいただきますようお願い申し上げます。
            なお、政府の発表等により運営オペレーション等を追加・変更させていただく場合がございますので、予めご了承ください。
            お客様のご理解とご協力を賜りますようお願い申し上げます。
          </v-card-text>
        </v-card>
      </v-dialog>
    </div>
    <div class="text-h4 font-weight-medium mt-12">About</div>
    <div class="text-subtitle-2">BB LABO.はこんなジムです</div>
    <p class="text-body-2 mt-8">
      コンセプトについての詳細を書く。コンセプトについての詳細を書く。コンセプトについての詳細を書く。コンセプトについての詳細を書く。コンセプトについての詳細を書く。コンセプトについての詳細を書く。コンセプトについての詳細を書く。コンセプトについての詳細を書く。コンセプトについての詳細を書く。
    </p>
    <div class="text-h5 font-weight-medium mt-10">Equipments</div>
    <div class="text-caption">多彩な設備が揃うスタジオ</div>
    <v-row class="mt-3">
      <v-col
        v-for="(item, i) in items"
        :key="i"
        class="d-flex child-flex"
        cols="6"
      >
        <v-img :src="item.src" aspect-ratio="1"> </v-img>
      </v-col>
    </v-row>
    <p class="text-body-2 mt-8">
      簡単に設備の説明を書く。簡単に設備の説明を書く。簡単に設備の説明を書く。簡単に設備の説明を書く。簡単に設備の説明を書く。簡単に設備の説明を書く。簡単に設備の説明を書く。
    </p>
    <div class="text-h5 font-weight-medium mt-10">Programs</div>
    <div class="text-caption">プロのメニューで効果を実感</div>
    <div class="mock mt-8"></div>
    <p class="text-body-2 mt-8">
      簡単にプログラムについてのアピールポイントを描く。簡単にプログラムについてのアピールポイントを描く。簡単にプログラムについてのアピールポイントを描く。簡単にプログラムについてのアピールポイントを描く。
    </p>
    <div class="text-center mt-8">
      <v-btn outlined tile to="/programs" class="font-weight-bold">もっと見る</v-btn>
    </div>
    <div class="text-center">
      <div class="text-h4 font-weight-medium mt-12">Price</div>
      <div class="text-subtitle-2">シンプルなチケットシステム<br>その都度買うから無理なく続けられる</div>
      <div class="mt-8"><span class="mr-10">1session</span><span>¥5,000 -</span></div>
      <div class="mt-4"><span class="mr-10">4sessions</span><span>¥18,000 -</span></div>
      <div class="mt-4"><span class="mr-10">8sessions</span><span>¥32,000 -</span></div>
      <div class="mt-4"><span class="mr-10">12sessions</span><span>¥50,000 -</span></div>
    </div>
    <div class="text-center">
      <div class="text-h4 font-weight-medium mt-12">Trial</div>
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
export default class About extends Vue {
  private dialog = false
  private items = [
    { src: require('../assets/images/pictures/pic1.jpg') },
    { src: require('../assets/images/pictures/pic2.jpg') },
    { src: require('../assets/images/pictures/pic3.jpg') },
    { src: require('../assets/images/pictures/pic4.jpg') },
  ]
}
</script>

<style lang="scss" scoped>
.mock {
  background-color: darkgray;
  height: 400px;
}
</style>
