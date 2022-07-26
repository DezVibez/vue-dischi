<template>


<div>
    <div id="albums" v-for="album in albums" :key="album.title">
    {{album.title}}
    </div>
    
</div>
  
</template>

<script>
import axios from 'axios';

export default {
name:"MainSection",
data(){
    return {
        albums: []
    }

    
},
created(){
    axios.get("https://flynn.boolean.careers/exercises/api/array/music")
    .then((response) => {
        this.albums = response.data.response
    })
}
}
</script>

<style>

</style>