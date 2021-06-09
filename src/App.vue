<template>
 <ul class="view">
   <li v-for="(item, i) in product" v-bind:key="i">{{product[i].title}}</li>
 </ul>
</template>

<script>
import vdata from './data.js'

export default {
  name: 'App',
  data(){
    return{
      product:vdata, 
    }
  }
 
}
</script>

<style>
  *{margin: 0; padding: 0;}
  li{list-style: none;}
  view{}
</style>
