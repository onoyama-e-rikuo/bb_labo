<template>
  <div class="fv-box" :style="{ height: windowHeight -56 + 'px' }">
    <div class="a font-weight-black text-h3">
      <p>WORK OUT WITH A PRO</p>
    </div>
    <div class="b text-subtitle-2">
      <p>プロだから知っている、本当に効果のあるトレーニング</p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {

  },
})
export default class Programs extends Vue {
  private windowHeight = 0

  private isClient = process.client

  created() {
    if (this.isClient) {
      window.addEventListener('resize', this.handleResize)
      this.handleResize()
    }
  }

  destroyed() {
    if (this.isClient) {
      window.removeEventListener('resize', this.handleResize)
    }
  }

  handleResize() {
    this.windowHeight = window.innerHeight
  }
}
</script>

<style lang="scss" scoped>
.fv-box {
  margin-top: 56px;
  height: 100%;
  background-color: darkgray;
  position: relative;
}
.b {
  background-color: white;
  width: 85%;
  position: absolute;
  bottom: 23%;
  padding-left: 16px;
  p {
    margin: 0;
  }
}
.a {
  margin-bottom: 5px;
  background-color: white;
  width: 85%;
  position: absolute;
  bottom: 30%;
  padding-left: 16px;
  p {
    margin: 0;
  }
}
</style>
