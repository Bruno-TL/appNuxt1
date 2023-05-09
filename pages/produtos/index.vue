<template>
  <div>
    <NuxtLink to="/produtos/produto-a">PRODUTO A </NuxtLink>
    <NuxtLink to="/produtos/produto-b">PRODUTO B </NuxtLink>
    <h1 class="text-lg font-bold">Produtos</h1>
    <div v-for="product in products" :key="product.id" class="border-b border-gray-400 py-3">
      <h2>{{ product.title }}</h2>
      <p>{{ product.body }}</p>
      <br>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam ipsam beatae, doloribus minima quos consequatur
      dignissimos! Sequi enim in vitae nesciunt quidem ratione tempora, quisquam maxime. Sed illum ex incidunt!</p>
  </div>
</template>

<script>
export default {
  data(){
    return {

    };
  },
  async asyncData({$axios}){
    const products = await $axios.$get('https://jsonplaceholder.typicode.com/posts?_limit=3')
    return{
      products,
    }
  },
}
</script>

<style></style>