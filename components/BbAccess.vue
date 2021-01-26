<template>
  <div class="text-center pa-6">
    <div class="blue--text font-weight-bold text--darken-4 text-caption">
      アクセス
    </div>
    <div class="text-h6 font-weight-medium">ACCESS</div>
    <v-row no-gutters>
      <v-col cols="12" sm="12" lg="6" offset-lg="3">
        <v-card flat>
          <v-img :src="img_src"></v-img>
          <div class="text-left text-body-2">
            <p>〒672-8051<br />兵庫県姫路市飾磨区清水2-103<br />高島ビル1F</p>
            <p>
              TEL: 080-8321-3587<br />営業時間: 10:00 ~ 19:00
              <br />定休日:火曜日
            </p>
            <p>駐車場2台あり</p>
          </div>
          <v-btn depressed color="primary">Google Mapで開く</v-btn>
          <v-row no-gutters>
            <v-col cols="12" sm="12" lg="6">
              <v-card flat tile>
                <div
                  class="text-body-1 blue--text font-weight-bold text--darken-4"
                >
                  バスでお越しの方
                </div>
                <p class="text-left text-body-2">
                  ・地下鉄日比谷線広尾駅2番出口より徒歩4分<br />
                  ・JR恵比寿駅西口より徒歩12分
                </p>
              </v-card>
            </v-col>
            <v-col cols="12" sm="12" lg="6">
              <v-card flat tile>
                <div
                  class="text-body-1 blue--text font-weight-bold text--darken-4"
                >
                  電車でお越しの方
                </div>
                <p class="text-left text-body-2">
                  ・渋谷駅東口58番乗り場から【都06新橋駅前行き】乗車→広尾5丁目下車徒歩1分<br />
                  ・目黒駅前2番乗り場から【黒77千駄ヶ谷駅行き・橋86新橋駅前行き・橋86東京タワー行き】乗車→天現寺橋
                  下車徒歩5分
                </p>
              </v-card>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class BbAccess extends Vue {
  private img_src: string = require('../assets/images/bb_building.png')
}
</script>

<style lang="scss"></style>
