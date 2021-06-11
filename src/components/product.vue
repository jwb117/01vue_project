<template>
<div>
    <img v-bind:src="product.image">
    <div>{{product.title}}
        <span @click="$emit('modalOpen', product.id)">[자세히보기]</span>
    </div>
    <div>{{product.price}}</div>
</div>


</template>

<script>
export default {
    name:'product',
    props:['product']
}
</script>

<style>

</style>