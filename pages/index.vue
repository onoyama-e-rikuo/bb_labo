<template>
  <div>
    <bb-firstview :style="{ height: windowHeight + 'px' }" />
    <bb-info />
    <v-row no-gutters>
      <bb-about />
      <bb-staff />
      <bb-menu />
      <bb-interview />
    </v-row>
    <bb-access />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import BbCarousels from '~/components/BbCarousels.vue'
import BbInfo from '~/components/BbInfo.vue'
import BbAbout from '~/components/BbAbout.vue'
import BbStaff from '~/components/BbStaff.vue'
import BbMenu from '~/components/BbMenu.vue'
import BbInterview from '~/components/BbInterview.vue'
import BbAccess from '~/components/BbAccess.vue'
import BbFirstview from '~/components/BbFirstview.vue'

@Component({
  components: {
    BbCarousels,
    BbInfo,
    BbAbout,
    BbStaff,
    BbMenu,
    BbInterview,
    BbAccess,
    BbFirstview,
  },
})
export default class Index extends Vue {
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
