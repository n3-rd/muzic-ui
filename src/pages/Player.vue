<template>
 <q-layout view="lHh lpr lFf">

    <div>
        <div class="stylish-underlay">

        </div>

      <q-header class="q-mt-xl q-px-md">
        <q-toolbar class="bg-transparent">
          <q-icon name="eva-arrow-ios-downward" class="q-mr-sm text-dark" size="sm"/>
          <q-toolbar-title class="text-center text-dark poppins-medium">Playing Now</q-toolbar-title>
          <q-icon name="eva-list" size="sm" />
        </q-toolbar>
      </q-header>

<div class="player-widgets q-pt-xl">
<AlbumCover class="q-pt-xl"/>

</div>
        
    </div>
 </q-layout>

</template>

<style lang="scss">
.stylish-underlay{
    width: 80vw;
    height: 50vh;
    border-radius: 0 0 15px 0;
    background-color: #B1F241;
    position: absolute;
}
.q-header{
    background: transparent;
}

</style>

<script>
import AlbumCover from '../components/player-assets/AlbumCover.vue';
export default {
    components: {
        AlbumCover
},
}
</script>