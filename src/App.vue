<template>
  <div id="app">

    <div>

      <MyHeader>
      </MyHeader>


      <MainSection class="p-1">

      </MainSection>

    </div>


    
  </div>
</template>

<script>
import MainSection from "./components/MainSection.vue"
import MyHeader from "./components/MyHeader.vue"

export default {
  name: 'App',
  components: {
    MainSection,
    MyHeader
  }
}
</script>

<style lang="scss">
@import "./assets/scss/style.scss";

#app{
  background-color: rgb(30,45,59)
}


</style>
