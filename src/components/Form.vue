<template>
  <h1>Meu formulário</h1>
  <form>
    <div>
      <input type="text" v-model="nome">
    </div>
    <div>
      <input type="text" v-model="email">
    </div>
    <InputSubmit @click="enviarFormulario($event)" />
  </form>
</template>

<script>
// import InputText from './form/InpuText.vue'
import InputSubmit from './form/InputSubmit.vue'

export default {
  components: {
    // InputText,
    InputSubmit
  },
  data() {
    return {
      nome: '',
      email: ''
    }
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault()

      const nome = this.nome
      const email = this.email

      console.log('Formulario enviado.')
      console.log({
        nome,
        email
      })
    }
  }
}
</script>