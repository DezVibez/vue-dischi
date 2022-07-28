<template>
  <div>
    <select name="" id="" >
      <option  disabled value="Seleziona un genere">Seleziona un genere</option>
      <option v-for="(album, index) in albums" :key="index" :value="album.genre">
        {{ album.genre }}
      </option>
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
  methods: {},
};
</script>

<style>
</style>