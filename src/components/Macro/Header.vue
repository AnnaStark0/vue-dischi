<template>
  <header class="py-3">
    <div class="container-fluid">
      <div class="row">
        <div class="col">

          <img src="../../assets/img/logo.png" alt="" />

        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/Variabili.scss";

header {
  background-color: $spotifyColor;

  img {
      width: 50px;
  }
}


</style>