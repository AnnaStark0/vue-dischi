<template>
  <div class="album my-3">
    <img
      src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg"
      alt=""
    />
    <h3 class="text-center my-2">NEW JERSEY</h3>
    <p class="text-center">
      Bon Jovi <br />
      1988
    </p>
  </div>
</template>

<script>
export default {
  name: "AlbumCard",
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