<template>
  <div class="container py-3">
      <div class="row">
          <div class="col">
              <SelectGen/>
          </div>
      </div>
    <div class="row">

      <div class="col-3" v-for="(album, index) in albums" :key="index">
          <AlbumCard :info="album"/>
      </div>

    </div>
  </div>
</template>

<script>
import axios from 'axios';

import AlbumCard from '../Commons/AlbumCard.vue';
import SelectGen from '../Commons/SelectGen.vue';

export default {
name: 'AlbumsList',
components: {
    AlbumCard,
    SelectGen
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