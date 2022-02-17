<template>
  <div>
    <h2>Esta é a descrição da pessoa: {{ nome }} </h2>
    <Info :email="email"/>
    <Form />
  </div>
</template>

<script>
import Info from './Info.vue'
import Form from './Form.vue'

export default {
  name: 'Pessoa',
  data() {
    return {
      nome: 'Eric',
      email: 'email@email.com'
    }
  },
  components: {
    Info,
    Form
  }
}
</script>