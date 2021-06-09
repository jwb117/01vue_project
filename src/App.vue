<template>
 <ul class="view">
   <li v-for="(item, i) in product" v-bind:key="i">{{product[i].title}}</li>
 </ul>

<banner />

</template>

<script>
import vdata from './data.js'
import 명작 from './components/banner.vue'

export default {
  name: 'App',
  data(){
    return{
      product:vdata, 
    }
  }, 
  components:{
    banner:명작
  }
 
}
</script>

<style>
  *{margin: 0; padding: 0;}
  li{list-style: none;}
  view{}
</style>
