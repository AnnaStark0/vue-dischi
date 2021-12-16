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
import axios from 'axios';

import AlbumCard from '../Commons/AlbumCard.vue';

export default {
name: 'AlbumsList',
components: {
    AlbumCard
},
data () {
return {
    albums: null
}
},
created () {

axios.get('https://flynn.boolean.careers/exercises/api/array/music')
  .then ((response) => {
    // handle success
    this.albums = response.data.response;
  })
  .catch(function (error) {
    // handle error
    console.log(error);
  });
}
};
</script>

<style>
</style>