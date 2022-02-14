<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Não estou trabalhando no momento.</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
      <li>JavaScript</li>
      <li>Node.JS</li>
      <li>Sequelize ORM</li>
    </ul>
    <p v-show="mostrar_email">Enviar email para: {{ email }}</p>
    <p>Para acessar meu portifóolio basta clicar <a v-bind:href="meu_link" target="_blank">aqui</a></p>
    <Picture />
  </div>
</template>

<script>
import Picture from './Picture.vue'

export default {
  name: 'Info',
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: true,
      email: 'eric@email.com',
      meu_link: 'http://www.google.com'
    }
  },
  components: {
    Picture
  }
}
</script>