<template>
  <div></div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import BbCarousels from '~/components/BbCarousels.vue'
import BbInfo from '~/components/BbInfo.vue'
import BbAbout from '~/components/BbAbout.vue'

@Component({
  components: {
    BbCarousels,
    BbInfo,
    BbAbout,
  },
})
export default class Index extends Vue {}
</script>
