<template>
  <div id="app">

    <div>

      <MyHeader>
      </MyHeader>


      <MainSection class="p-1" :albums= "albums">

      </MainSection>

    </div>


    
  </div>
</template>

<script>
import MainSection from "./components/MainSection.vue"
import MyHeader from "./components/MyHeader.vue"
import axios from "axios"

export default {
  name: 'App',
  components: {
    MainSection,
    MyHeader
  },
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

<style lang="scss">
@import "./assets/scss/style.scss";

#app{
  background-color: rgb(30,45,59)
}


</style>
