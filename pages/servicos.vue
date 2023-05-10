<template>
  <div>
    <h1 class="text-lg font-bold">Serviços</h1>
    <NuxtLink to="/servicos/landingPage">
      Landing Page
    </NuxtLink>
    <NuxtLink to="/servicos/marketing-digital">
      Marketing Digital
    </NuxtLink>
    <br> <br>
    <div v-if="$fetchState.pending">
      Carregando ...
    </div>
    <div v-else>
      <div v-for="service in services" :key="service.id" class="border-b border-gray-400 py-4">
        {{ service.username }}
      </div>
    </div>

    <br> <br>

    <NuxtChild />
  </div>
</template>

<script>
export default {
  data() {
    return {
      services: []
    }
  },
  async fetch() {
    this.services = await this.$axios.$get('https://jsonplaceholder.typicode.com/users?_limit=3')
  },
  head(){
    return {
      title:'Serviços',
      meta: [
        { hid: 'description', name:'description', content: 'Minha descrição do serviços'}
      ],
      bodyAttrs: {
        class:'bg-gray-400'
      }
    }
  }
}
</script>

<style></style>