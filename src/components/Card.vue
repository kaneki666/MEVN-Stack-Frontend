<template>
  <div class="card" style="width: 100%; height:100%;">
    <div class="card-body">
        <router-link tag="a" :to="{name: 'product', params: {id: product._id}}">
            <img class="card-img-top" :src="product.image" :alt="product.name">
        </router-link>
        <h5 class="card-title text-name">{{ product.name }}</h5>
        <p><span class="font-weight-bold">Category</span>: {{ product.category }}</p>
        <p class="card-text">{{ product.description.substring(0, 50) }}</p>
        <p class="font-weight-bold">${{ product.price }}</p>
        <router-link tag="a" class="btn btn-outline-danger mr-2" :to="{ name: 'product', params: { id: product._id }}">Desciption</router-link>
        <button class="btn btn-danger" @click="addToCart(product)">Buy Now</button>
    </div>
</div>
</template>

<script>
import mixins from '@/mixins/mixins';
export default {
    props: ['product'],
    mixins: [mixins]
}
</script>

<style scoped>
.card-title {
        cursor: pointer;
    }
.text-name{
    color: #FF512F;
}


</style>
