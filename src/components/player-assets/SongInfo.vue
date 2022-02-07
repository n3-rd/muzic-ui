<template>
  <div>
    <div class="song-title q-mr-lg">{{ title }}</div>
    <div class="song-artist">{{ artist }}</div>
  </div>
</template>

<style lang="scss">
.song-title {
  font-size: 1.5rem;
  font-weight: bold;
  color: #fff;
  font-family: poppinsmedium;
  // margin-top: 10px;
  opacity: 0.8;
  white-space: nowrap;
}
.song-artist {
  font-size: 1rem;
  color: #fff;
  font-family: poppinsmedium;
  opacity: 0.6;
  white-space: nowrap;
}
</style>

<script>
export default {
  data() {
    return {
      artist: localStorage.getItem("storedSongDetailsArtist"),
      title: localStorage.getItem("storedSongDetailsTitle"),
    };
  },
  methods: {
    updateMetaData: function () {
      setInterval(() => {
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
