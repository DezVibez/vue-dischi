<template>

<div id="spotify-bar">

    <SearchBar>

    </SearchBar>



    

</div>
  
</template>

<script>
import SearchBar from "./SearchBar.vue"

export default {
name: "MyHeader",
components: {

    SearchBar
},
props: {options: Array},
data() {
    return{
      option: {
        value: this.options.genre,

      }
     }
    },
computed:{},
   
methods: {}
    
    
}

</script>

<style lang="scss" scoped>

#spotify-bar{
height: 50px;
width: 100%;
background-color: rgb(46,58,70);
margin-bottom: 50px;
display: flex;
justify-content: center;
align-items: center;
}

</style>