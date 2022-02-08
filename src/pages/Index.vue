<template>
  <q-page class="">
    <div>
      <q-list>
        <div
          v-for="song in songs"
          :key="song.songId"
          class="song"
          @click="storePlayerDetails(song.songArt, song.artist, song.songTitle)"
        >
          <q-item>
            <q-item-section avatar>
              <!-- <q-img src="~assets/for.jpg" :ratio="1"/> -->
              <img :srcset="song.songArt" class="song-art" />
            </q-item-section>
            <q-item-section>
              <q-item-label class="song-name poppins-medium" lines="1">{{
                song.songTitle
              }}</q-item-label>
              <q-item-label caption class="text-grey-1 song-artist">{{
                song.artist
              }}</q-item-label>
            </q-item-section>
          </q-item>
        </div>
      </q-list>
    </div>

    <IndexFooter />
    <router-link to="/Player">Player</router-link>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import { uid } from "quasar";
import IndexFooter from "components/IndexFooter.vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    IndexFooter,
  },
  data() {
    return {
      songs: [
        {
          artist: "MØ",
          songTitle: "Way Down",
          songArt: "img/1.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Nicki Minaj",
          songTitle: "Chun Li",
          songArt: "img/2.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Juice Wrld",
          songTitle: "Wishing Well",
          songArt: "img/3.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Mayrics",
          songTitle: "Lady",
          songArt: "img/4.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Major Lazer",
          songTitle: "Get Free (feat. Amber Coffman)",
          songArt: "img/5.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "MØ",
          songTitle: "Kamikaze",
          songArt: "img/6.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Whethan",
          songTitle: "Sunshine (With The Knocks)",
          songArt: "img/7.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "MØ",
          songTitle: "Goosebumps",
          songArt: "img/8.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Rick Astley",
          songTitle: "Never Gonna Give You Up",
          songArt: "img/9.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Billie Eilish",
          songTitle: "Bury A Friend",
          songArt: "img/10.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Kanye West",
          songTitle: "Selah",
          songArt: "img/11.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Eminem",
          songTitle: "Gnat",
          songArt: "img/12.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Major Lazer, Sia, Labrinth & Diplo",
          songTitle: "Titans",
          songArt: "img/13.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Khalid",
          songTitle: "Saturday Nights",
          songArt: "img/14.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "MØ",
          songTitle: "Blur",
          songArt: "img/15.jpg 9x",
          songId: "uid()",
        },
        {
          artist: "Bob Marley & The Wailers",
          songTitle: "Three Little Birds",
          songArt: "img/16.jpg 9x",
          songId: "uid()",
        },
         {
          artist: "James Blunt",
          songTitle: "Goodbye My Lover",
          songArt: "img/17.jpg 9x",
          songId: "uid()",
        },
      ],
    };
  },
  methods: {
    storePlayerDetails: function (image, artist, title) {
      localStorage.setItem("storedSongDetailsImage", image);
      localStorage.setItem("storedSongDetailsArtist", artist);
      localStorage.setItem("storedSongDetailsTitle", title);
      console.log(localStorage.getItem("storedSongDetails"));
    },
    getTopCharts: function(){
      fetch('https://api.deezer.com/chart/0/tracks')
      .then(response => response.json())
    }
  },
});
</script>

<style lang="scss">
.song-name {
  font-size: 1.2rem;
}
img {
  width: 100%;
}
.song-art {
  border-radius: 15px;
}
// .song{
//   z-index: 9999;
// }
</style>
