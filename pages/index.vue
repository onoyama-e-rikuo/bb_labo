<template>
  <div>
    <bb-carousels />
    <bb-info />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import BbCarousels from '~/components/BbCarousels.vue'
import BbInfo from '~/components/BbInfo.vue'

@Component({
  components: {
    BbCarousels,
    BbInfo,
  },
})
export default class Index extends Vue {}
</script>
