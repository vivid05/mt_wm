<template>
  <div id="App">
      <router-view :currentCity='currentCity' @changeCity="change"></router-view> 
  </div>
</template>

<script>
export default {
    name:'App',
    data(){
      return {
        currentCity:'安庆'
      }
    },
    methods:{
      change(city){
        this.currentCity=city
      }
    }
}
</script>

<style>

</style>