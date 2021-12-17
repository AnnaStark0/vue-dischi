<template>
<main>

<AlbumsList/>
</main>
</template>

<script>

import AlbumsList from '../Sections/AlbumsList.vue';

export default {
name: 'Main',
components: {

  AlbumsList
}
}
</script>

<style lang="scss" scoped>
main {
  background-color: black;
}

</style>