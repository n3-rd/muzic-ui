<template>
  <div>
    <q-footer class="q-px-md">
      <div class="row poppins-medium">
        <div class="col-2">
          <router-link to="/Player">
            <img srcset="img/1.jpg 9x" class="indexImg" />
          </router-link>
        </div>
        <div class="col-6">
          <router-link to="/Player">
            <div class="q-ml-md">
              <span class="index-song"> Way Down </span>
              <br />
              <span class="index-artist"> MØ </span>
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
