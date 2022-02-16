<template>
  <div>
    <h1>Hello!!</h1>
    <p>Meu nome é {{ nome }}</p>
    <MultiplosEventos />
  </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'

export default {
  name: 'PrimeiroComponente',
  components: {
    MultiplosEventos
  },
  data() {
    return {
      nome: "Eric"
    }
  }
}
</script>

