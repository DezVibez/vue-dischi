<template>
<div>
    
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
        console.log(response.data)

        this.albums = response.data.response
    })
}
}
</script>

<style>

</style>