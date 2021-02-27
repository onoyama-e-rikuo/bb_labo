<template>
  <div>
    <div class="text-h6 font-weight-medium mt-10">
      兵庫県<br />姫路市飾磨区<br />清水2-103
    </div>
    <div class="text-h6 font-weight-medium mt-4">駐車場2台あり</div>
    <div class="mock my-10"></div>
    <bb-carousels></bb-carousels>
    <div class="text-center">
      <div class="text-h6 font-weight-medium mt-10">お車でお越しの場合</div>
      <p class="text-body-2 mt-4">
        簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。
      </p>
    </div>
    <div class="text-center">
      <div class="text-h6 font-weight-medium mt-10">電車でお越しの場合</div>
      <p class="text-body-2 mt-4">
        簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。簡単な道案内を書く。
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import BbCarousels from "~/components/BbCarousels.vue";

@Component({
  components: {
    BbCarousels,
  },
})
export default class Access extends Vue {
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
