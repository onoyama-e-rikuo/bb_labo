<template>
  <div>
    <bb-carousels />
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
export default class Index extends Vue {}
</script>
