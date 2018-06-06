<template>
 <div>
   <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"></app-header>
   <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>
   <app-footer v-bind:title="title"></app-footer>
   
 </div>
</template>

<script>
import Header from './components/Header.vue'

import Ninjas from './components/Ninjas.vue'
import Footer from './components/Footer.vue'

export default {
  components: {
    'app-header': Header,
    'app-footer': Footer,
    'app-ninjas': Ninjas
  },
  data() {
    return {
      ninjas: [
        {name: 'Andi', speciality: 'Vue Components', show: false},
        {name: 'Crystal', speciality: 'HTML Wizards', show: false},
        {name: 'Hitoshi', speciality: 'Click EVENTS', show: false}
      ],
      title: "Vue Ninjas"
    }
  },
  methods: {
    updateTitle: function(updateTitle){
      this.title = updateTitle;
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>