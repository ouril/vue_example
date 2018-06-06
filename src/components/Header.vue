<template>
<div>
  <header>
  <h1 v-on:click="changeTitle">{{ title }}</h1>
  </header>
  
</div>
</template>

<script>
import { bus } from '../main'

export default {
props:{
  title:{
    type: String
  }
},
data() {
  return {
    title: 'Vue Gruzdev'
  }
},
methods: {
  changeTitle: function(){
    //this.$emit('changeTitle', "Viiii!!!");
    this.title = 'Vuuu!!!'
    bus.$emit('titleChanged', 'Vuuu!!!')
  }
}

 }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
    background: lightgreen;
    padding: 10px
  }
h1 {
  color: #222;
  text-align: center;
}
</style>
