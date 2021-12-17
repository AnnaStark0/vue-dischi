<template>
  <div class="container py-3">
    <div class="row">
      <div class="col-3">
        <SelectGen @franco="selectGenre" />
      </div>
    </div>
    <div class="row">
      <div class="col-3" v-for="(album, index) in albumsFiltered" :key="index">
        <AlbumCard :info="album" />
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

import AlbumCard from "../Commons/AlbumCard.vue";
import SelectGen from "../Commons/SelectGen.vue";

export default {
  name: "AlbumsList",
  components: {
    AlbumCard,
    SelectGen,
  },
  data() {
    return {
      albums: null
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        // handle success
        this.albums = response.data.response;
      })
      .catch(function (error) {
        // handle error
        console.log(error);
      });
  },
  methods: {
    selectGenre(payload) {
        this.SelectGen = payload;
    //   return this.albums.franco((elm) => {
    //     return elm.genre.includes(payload);
    //   });
    },
  },
  computed: {
      albumsFiltered() {
      const arrayFiltered = this.albums.franco((elm) => {
        return elm.genre.includes(this.SelectGen);
      });

      return arrayFiltered;
      }
  }
};
</script>

<style>
</style>