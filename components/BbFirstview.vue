<template>
  <div class="fv-box">
    <bb-carousels />
    <div class="fv-title">
      <p>BODYMAKE×<br />BASEBALLMETHOD</p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import BbCarousels from '~/components/BbCarousels.vue'
@Component({
  components: {
    BbCarousels,
  },
})
export default class BbFirstview extends Vue {
  private logoCube = require('../assets/images/bb_logo_cube_white.svg')
}
</script>

<style lang="scss">
.fv-box {
  height: 100%;
  background-color: #364e8a;
  position: relative;
  display: flex;
}

.fv-title {
  align-self: flex-end;
  display: flex;
  font-size: 3rem;
  p {
    color: #ffffff;
    font-weight: 800;
    writing-mode: vertical-rl;
    line-height: 1em;
  }
}
</style>
