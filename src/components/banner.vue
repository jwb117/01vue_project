<template>
  <div class="banner">
    {{text}}
  </div>
</template>

<script>
export default {
    name:'banner',
    data(){
        return{
            text:'hello'
        }
    }
}
</script>

<style>
    .banner{height: 200px; width: 100%; background: skyblue; display: flex; justify-content: center; align-items: center;}
</style>