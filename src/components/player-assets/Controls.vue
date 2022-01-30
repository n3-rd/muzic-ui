<template>
  <div class="q-px-xl">
    <q-linear-progress
      dark
      rounded
      size="6px"
      :value="0.4"
      color="danger"
      class="q-mt-sm"
    />
    <div class="timer row q-mt-sm">
      <div class="current-time col-6">0:33</div>
      <div class="total-time text-right col-6">3:21</div>
    </div>

    <div class="q-mt-lg">
      <div class="player-controls row">
        <div class="col-4">
          <!-- <q-icon name="eva-rewind-left" size="md" /> -->
          <q-btn icon="eva-rewind-left" size="lg" round @click="nextSong()" />
        </div>
        <div class="col-4 text-center">
          <q-btn class="play-control">
            <q-icon
              name="eva-play-circle"
              class="play-control-icon"
              size="6em"
            />
          </q-btn>
          <!-- <div class="play-control">
                 <q-btn text-color="black" icon="eva-play-circle" size="37px" dense align="between" round/>
                 </div> -->
        </div>
        <div class="col-4">
          <!-- <q-icon name="eva-rewind-right" size="md"/> -->
          <q-btn icon="eva-rewind-right" size="lg" round />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueEvents from "vue-events";
export default {
  data() {
    return {};
  },
  methods: {
    nextSong: function () {
      //  console.log(this.$.parent.parent.components.AlbumCover.methods.nextButtonClicked())
      this.$.parent.parent.components.AlbumCover.methods.nextButtonClicked();
    },
  },
};
</script>

<style lang="scss">
#q-app
  > div
  > div
  > div.player-widgets.q-pt-xl
  > div:nth-child(3)
  > div
  > div.q-linear-progress__model.absolute-full.q-linear-progress__model--with-transition.q-linear-progress__model--determinate {
  background-color: #b1f241;
}
.timer {
  font-family: poppinsmedium;
  opacity: 0.8;
  .total-time {
    text-align: right;
  }
}
.player-controls {
  margin: 0 auto;
  text-align: center;
  * {
    align-self: center;
  }
}
.play-control {
  margin: 0 auto;
  .play-control-icon {
    color: #b1f241;
  }
  // background: #B1F241;
}
</style>
