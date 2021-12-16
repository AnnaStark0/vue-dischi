<template>
  <div class="container my-5">
    <div class="row">
      <div class="col-12 col-sm-5 col-md-3">
          <AlbumCard/>
      </div>

            <div class="col-12 col-sm-5 col-md-3">
          <AlbumCard/>
      </div>

            <div class="col-12 col-sm-5 col-md-3">
          <AlbumCard/>
      </div>

            <div class="col-12 col-sm-5 col-md-3">
          <AlbumCard/>
      </div>

            <div class="col-12 col-sm-5 col-md-3">
          <AlbumCard/>
      </div>

    </div>
  </div>
</template>

<script>
import AlbumCard from '../Commons/AlbumCard.vue';

export default {
name: 'AlbumsList',
components: {
    AlbumCard
}
};
</script>

<style>
</style>