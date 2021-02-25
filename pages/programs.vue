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
      <div class="d-flex justify-space-around align-center">
        <div>
          <div class="text-caption text-center">初めての方</div>
          <v-btn large outlined tile @click="trialClass = true"
          ><span class="text-caption font-weight-bold">Trial Class</span></v-btn
          >
        </div>
        <div>
          <div class="text-caption text-center">2回目以降の方</div>
          <v-btn large outlined tile @click="trialClass = false"
          ><span class="text-caption font-weight-bold"
          >Regular Class</span
          ></v-btn
          >
        </div>
      </div>
      <trial-class v-if="trialClass"/>
      <regular-class v-else/>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import TrialClass from "~/components/TrialClass.vue";
import RegularClass from "~/components/RegularClass.vue";

@Component({
  components: {
    TrialClass,
    RegularClass,
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

  private trialClass = true
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
