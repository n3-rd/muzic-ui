<template>
  <div>
    <q-footer class="q-px-md">
      <div class="row poppins-medium q-pt-lg">
        <div class="col-2">
          <router-link to="/Player">
            <img :srcset="songArt" class="indexImg" />
          </router-link>
        </div>
        <div class="col-6">
          <router-link to="/Player">
            <div class="q-ml-md">
              <!-- <span class="index-song" lines="1"> {{title}} </span>
              <br />
              <span class="index-artist" lines="1"> {{artist}} </span> -->

              <q-item-section>
                <q-item-label class="song-name poppins-medium" lines="1">{{
                  title
                }}</q-item-label>
                <q-item-label caption class="text-grey-1 song-artist">{{
                  artist
                }}</q-item-label>
              </q-item-section>
            </div>
          </router-link>
        </div>
        <div class="col-4 index-buttons">
          <q-btn icon="eva-rewind-left" size="md" round />
          <q-btn icon="eva-play-circle" size="md" round />
          <q-btn icon="eva-rewind-right" size="md" round />
        </div>
      </div>
    </q-footer>
  </div>
</template>

<style lang="scss">
.index-song {
  font-size: 1.5rem;
}
.index-artist {
  font-size: 1.2rem;
  opacity: 0.8;
}
.index-buttons {
  align-self: center;
}
a {
  text-decoration: none;
}
</style>

<script>
export default {
  data() {
    return {
      songArt: localStorage.getItem("storedSongDetailsImage"),
      artist: localStorage.getItem("storedSongDetailsArtist"),
      title: localStorage.getItem("storedSongDetailsTitle"),
    };
  },
  methods: {
    updateMetaData: function () {
      setInterval(() => {
        (this.songArt = localStorage.getItem("storedSongDetailsImage")),
          (this.artist = localStorage.getItem("storedSongDetailsArtist")),
          (this.title = localStorage.getItem("storedSongDetailsTitle"));
      }, 1000);
    },
  },
  mounted() {
    this.updateMetaData();
  },
};
</script>
