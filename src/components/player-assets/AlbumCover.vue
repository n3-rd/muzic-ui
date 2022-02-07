<template>
    <div>
        <!-- <div v-if="album"> -->
            <album>
<div>

            <img :srcset="albumCover" class="album-cover" />
        </div>
                </album>
            
        
    </div>
</template>

<script>
import VueEvents from 'vue-events'
const albumCover = document.querySelector('.album-cover');

export default {
    data(){
      return{
       albumCover: localStorage.getItem('storedSongDetailsImage'),
      }
    },
    methods: {
        nextButtonClicked: function(){
        // this.album.style.marginLeft = '23px';
        albumCover.style.display = 'none'
        console.log(albumCover.style.display)

        },
        updateMetaData: function(){
  setInterval(()=>{
    this.songArt = localStorage.getItem('storedSongDetailsImage')
  }, 1000)
  
}
    },
 mounted(){
     this.updateMetaData();
 }
}
</script>

<style lang="scss">
.album-cover{
    // background: red;

    height: 41vh;
    width: 83vw;
    margin: 30px auto;
    border-radius: 20px;
    position: relative;
        display: block;
}
</style>