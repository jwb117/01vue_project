<template>

<banner/>

<!-- <div class="black-bg" v-if="proView == true">
  <div class="white-bg">
    <img v-bind:src="product[proNum].image" alt="">
     <div>{{product[proNum].title}}</div>
     <div>{{product[proNum].price}}</div>
     <div>{{product[proNum].content}}</div>
     <button v-on:click="proView=false">닫기</button>
  </div>
</div> -->
<modal v-bind:product="product" :proView="proView" v-bind:proNum="proNum" @modalClose="proView=false"/>

<!-- <div>
 <ul class="view">
   <li v-for="(item, i) in product" v-bind:key="i">
     <img v-bind:src="product[i].image" alt="">
     <div>{{product[i].title}} <span v-on:click="proView=true; proNum=i">[상세보기]</span></div>
     <div>{{product[i].price}}</div>
     </li>
 </ul> -->
<product :product="product[i]" v-for="(item, i) in product" v-bind:key="i" @modalOpen="proView=true; proNum=$event"/>

<banner></banner>

</template>

<script>
import vdata from './data.js'
import banner from './components/banner.vue'
import modal from './components/modal.vue'
import product from './components/product.vue'

export default {
  name: 'App',
  data(){
    return{
      proNum:0,
      proView:false,
      product:vdata, 
      
    }
  }, 
  components:{
   banner:banner,
   modal:modal,
   product:product,
  }
 
}
</script>

<style>
  html, body{height: 100%; }
  *{margin: 0; padding: 0;}
  li{list-style: none;}
  img{width: 100%;}
  .view li{margin-bottom: 20px;}
  .black-bg{position: fixed; width: 100%; background: rgba(0,0,0,0.5); top:0; height: 100%; display: flex; justify-content: center; align-items: center; }
  .white-bg{width: 80%; background: #fff; border-radius: 5px; padding: 20px; }

</style>
