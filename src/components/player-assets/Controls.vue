<template>
    <div class="q-px-xl">
         <q-linear-progress dark rounded size="6px" :value=0.4 color="danger" class="q-mt-sm" />
         <div class="timer row q-mt-sm">
             <div class="current-time col-6">0:33</div>
             <div class="total-time text-right col-6">3:21</div>
         </div>

            <div class="q-mt-lg">
   <div class="player-controls row">
             <div class="col-4">
                 <q-icon name="eva-rewind-left" size="md" />
             </div>
             <div class="col-4">
                 <q-icon class="play-control" name="eva-play-circle"/>
             </div>
             <div class="col-4">
                 <q-icon name="eva-rewind-right" size="md"/>
             </div>
         </div>
            </div>
      
    </div>
</template>

<style lang="scss">
#q-app > div > div > div.player-widgets.q-pt-xl > div:nth-child(3) > div > div.q-linear-progress__model.absolute-full.q-linear-progress__model--with-transition.q-linear-progress__model--determinate{
    background-color: #B1F241;
}
.timer{
    font-family: poppinsmedium;
opacity: .8;
.total-time{
    text-align: right;
}
}
.player-controls{
    margin: 0 auto;
    text-align: center;
    *{
    align-self: center;
        
    }
}
.play-control{
    color: #B1F241;
    font-size: 6em;
}
</style>