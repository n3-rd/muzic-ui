<template>
  <q-layout view="lHh lpr lFf">
    <div class="player">
      <div class="stylish-underlay"></div>

      <q-header class="q-mt-xl q-px-md">
        <q-toolbar class="bg-transparent">
          <router-link to="/">
            <q-icon
              name="eva-arrow-ios-downward"
              class="q-mr-sm text-dark"
              size="sm"
            />
          </router-link>
          <q-toolbar-title class="text-center text-dark poppins-medium"
            >Playing Now</q-toolbar-title
          >
          <q-icon name="queue_music" size="sm" />
        </q-toolbar>
      </q-header>

      <div class="player-widgets q-pt-xl">
        <AlbumCover class="q-pt-xl" />
        <SongInfo class="q-pt-sm q-px-xl" />

        <Controls />
        <Footer />
      </div>
    </div>
  </q-layout>
</template>

<style lang="scss">
.stylish-underlay {
  width: 80vw;
  height: 50vh;
  border-radius: 0 0 15px 0;
  background-color: #b1f241;
  position: absolute;
}
.q-header {
  background: transparent;
}
.player {
  max-height: 100vh;
}
</style>

<script>
import AlbumCover from "../components/player-assets/AlbumCover.vue";
import SongInfo from "../components/player-assets/SongInfo.vue";
import Controls from "../components/player-assets/Controls.vue";
import Footer from "../components/player-assets/Footer.vue";
export default {
  components: {
    AlbumCover,
    SongInfo,
    Controls,
    Footer,
  },
};
</script>
