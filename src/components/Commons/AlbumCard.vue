<template>
  <div class="album my-3">
    <img :src="info.poster" alt="">
    <h3 class="text-center my-2">{{info.title}}</h3>
    <p class="text-center">
      {{info.author}} <br />
      {{info.year}}
    </p>
  </div>
</template>

<script>
export default {
  name: "AlbumCard",
  props: {
     info: Object 
  }
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/Variabili.scss";

.album {
  padding: 20px 20px 50px 20px;

  background-color: $spotifyColor;

  border-radius: 5px;

  img {
    width: 100%;
  }

  h3 {
    color: white;
  }

  p {
      color: lightgrey;
  }
}
</style>