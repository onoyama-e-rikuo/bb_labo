<template>
  <div class="fv-box"></div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import BbCarousels from '~/components/BbCarousels.vue'
@Component({
  components: {
    BbCarousels,
  },
})
export default class BbFirstview extends Vue {}
</script>

<style lang="scss">
.fv-box {
  height: 100%;
  background-color: darkgray;
  position: relative;
  display: flex;
}
</style>
