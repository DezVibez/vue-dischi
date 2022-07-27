<template>

<div id="spotify-bar">

    <select name="" id="">
        <option v-for="option in options" :value="option.value" :key="option.title">
        {{ option.text }}
  </option>
    </select>



    

</div>
  
</template>

<script>
export default {
name: "MyHeader",
props: {options: Array},
data() {
    return{
      
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