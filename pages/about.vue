<template>
  <div>
    <v-img contain :src="img_src" height="300"></v-img>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {},
})
export default class About extends Vue {
  private img_src: string = require('../assets/images/b.svg')
}
</script>
