<template>
<div>
    
</div>
  
</template>

<script>
import axios from 'axios';

export default {
name:"MainSection",
created(){
    axios.get("https://flynn.boolean.careers/exercises/api/array/music")
    .then((response) => {
        console.log(response.data)
    })
}
}
</script>

<style>

</style>