<template>
  <div>
    <div class="bg-gray-100 ">
        <div class="container mx-auto flex items-center space-x-4 h-10 mb-10">
            <NuxtLink :to="{name: 'a-empresa'}">A empresa</NuxtLink>
            <NuxtLink to="/servicos">Serviços</NuxtLink>
        </div>
    </div>
    <div>
        <div class="container  mx-auto">
            <h1 class="text-lg font-bold">Serviços</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam ipsam beatae, doloribus minima quos consequatur dignissimos! Sequi enim in vitae nesciunt quidem ratione tempora, quisquam maxime. Sed illum ex incidunt!</p>
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>