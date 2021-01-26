<template>
  <v-carousel
    cycle
    height="250"
    hide-delimiter-background
    show-arrows-on-hover
    delimiter-icon="mdi-minus"
  >
    <v-carousel-item v-for="(item, i) in items" :key="i">
      <v-img :src="item.src" height="100%"> </v-img>
    </v-carousel-item>
  </v-carousel>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class BbCarousels extends Vue {
  private items = [
    { src: require('../assets/images/pictures/pic1.jpg') },
    { src: require('../assets/images/pictures/pic2.jpg') },
    { src: require('../assets/images/pictures/pic3.jpg') },
    { src: require('../assets/images/pictures/pic4.jpg') },
    { src: require('../assets/images/pictures/pic5.jpg') },
  ]
}
</script>

<style lang="scss"></style>
