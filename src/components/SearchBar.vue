<template>
  <div>
    <select name="" id="" v-model="searchedGenre">
      <option  disabled>Seleziona un genere</option>
      <option value="rock">rock</option>
      <option value="pop">pop</option>
      <option value="jazz">jazz</option>
      <option value="metal">metal</option>
      
    </select>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  props: {
    albums: Array,
  },
  data() {
    return {
      searchedGenre: "",
    };
  },
  methods: {
    
  },
};
</script>

<style>
</style>