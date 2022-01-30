<template>
    <div>
        <!-- <div v-if="album"> -->
            <album v-model="album">
<div class="album-cover">

                
        <!-- </div> -->
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
       album: true
      }
    },
    methods: {
        nextButtonClicked: function(){
        // this.album.style.marginLeft = '23px';
        albumCover.style.display = 'none'
        console.log(albumCover.style.display)

        }
    },
    // events: {
    //     'nextButtonClickedEvent'(){
    //         this.nextButtonClicked()
    //     }
    // }
}
</script>

<style lang="scss">
.album-cover{
    // background: red;

    height: 45vh;
    width: 80vw;
    margin: 30px auto;
    border-radius: 20px;
    position: relative;
}
</style>