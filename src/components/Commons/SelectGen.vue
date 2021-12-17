<template>
  <div class="select-gen">
    <select v-model="selectVal" class="form-select form-select-sm" aria-label="Default select example" @change="$emit('select', selectVal)">
      <option selected>Open this select menu</option>
      <option value="1">Rock</option>
      <option value="2">Pop</option>
      <option value="3">Metal</option>
      <option value="4">Jazz</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "SelectGen",
  data() {
      return {
          selectVal: '', 
      }
  }
};
</script>

<style lang="scss" scoped>
</style>