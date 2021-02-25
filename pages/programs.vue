<template>
  <div>
    <div class="fv-box" :style="{ height: windowHeight - 56 + 'px' }">
      <div class="program-title font-weight-medium text-h3">
        <p>Programs</p>
      </div>
      <div class="program-subtitle text-subtitle-2">
        <p>補足メッセージあればここに書く</p>
      </div>
    </div>
    <div class="px-6 my-8">
      <training-menu />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import TrainingMenu from '~/components/TrainingMenu.vue'

@Component({
  components: {
    TrainingMenu,
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

.program-title {
  margin-bottom: 5px;
  background-color: white;
  width: 65%;
  position: absolute;
  top: 10%;
  padding-left: 16px;
  p {
    margin: 0;
  }
}

.program-subtitle {
  background-color: white;
  width: 65%;
  position: absolute;
  top: 18%;
  padding-left: 16px;
  p {
    margin: 0;
  }
}
</style>
