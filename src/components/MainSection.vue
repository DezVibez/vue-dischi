<template>


<div class="album-container">
    <div class="album-column gy-2" >
        <div class="album" v-for="album in albums" :key="album.title">
            <img :src="album.poster" :alt="album.title" class="img-fluid">
            <h4 >{{album.title}}</h4>
            <h6 >{{album.author}}</h6>
        
            <span>{{album.year}}</span><br>
            <span>{{album.genre}}</span>
        </div>
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

<style lang="scss" scoped>

.album-container {
    max-width: 70%;
    margin: 0 auto;
   flex-wrap:wrap
}


.album{
height: 400px;
width: 18%;
margin: 10px 0;
text-align: center;
background-color: rgb(46,58,70)
}

.album-column{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}

.album h4{
font-size: 20px;
margin: 25px 0;
color: white;
}

.album h6{
color: white;
font-size: 16px;
margin: 10px 0;
}

.album span{
    color: rgb(89,106,120);
}


</style>