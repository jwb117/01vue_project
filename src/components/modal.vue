<template>
  <div class="black-bg" v-if="proView == true">
  <div class="white-bg">
    <img v-bind:src="product[proNum].image" alt="">
     <div>{{product[proNum].title}}</div>
     <div>{{product[proNum].price.toLocaleString()}}원</div>
     <div>{{product[proNum].content}}</div>
     <button v-on:click="$emit('modalClose')">닫기</button>
  </div>
</div>
</template>

<script>
export default {
    name:'modal', 
    props:['proView', 'product', 'proNum']

}
</script>

<style>

</style>