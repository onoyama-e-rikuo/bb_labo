<template>
  <div>
    <v-img contain :src="img_src" height="300"></v-img>
    <bb-info />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import BbInfo from "~/components/BbInfo.vue";

@Component({
  components: {BbInfo,},
})
export default class About extends Vue {
  private img_src: string = require('../assets/images/b.svg')
}
</script>
