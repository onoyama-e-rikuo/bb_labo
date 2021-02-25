<template>
  <div>
    <firstview :style="{ height: windowHeight -56 + 'px' }" />
    <about />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Firstview from '~/components/Firstview.vue'
import About from "~/components/About.vue";

@Component({
  components: {
    Firstview,
    About,
  },
})
export default class Index extends Vue {
  private dialog = false
  private windowHeight = 0

  private isClient = process.client

  created() {
    if (process.client) {
      window.addEventListener('resize', this.handleResize)
      this.handleResize()
    }
  }

  destroyed() {
    if (process.client) {
      window.removeEventListener('resize', this.handleResize)
    }
  }

  handleResize() {
    this.windowHeight = window.innerHeight
  }
}
</script>
