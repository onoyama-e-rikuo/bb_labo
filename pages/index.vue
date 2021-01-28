<template>
  <div>
    <bb-firstview style="height: 100vh" />
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
export default class Index extends Vue {}
</script>
