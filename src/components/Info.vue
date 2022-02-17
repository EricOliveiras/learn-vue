<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Não estou trabalhando no momento.</p>
    <p>Utilizo as seguintes tecnologias BackEnd:</p>
    <ul>
      <li v-for="(technolgy, index) in technolgies" v-bind:key="index">
        {{ technolgy }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias FrontEnd:</p>
    <ul>
      <li v-for="technolgy in tech_front" :key="technolgy.id">
        {{ technolgy.language }}
      </li>
    </ul>
    <div>
      <button @click="showEmail">{{ texto_botao }}</button>
    </div>
    <p v-show="mostrar_email">Enviar email para: {{ email }}</p>
    <p>Para acessar meu portifóolio basta clicar <a v-bind:href="meu_link" target="_blank">aqui</a></p>
    <Picture />
  </div>
</template>

<script>
import Picture from './Picture.vue'

export default {
  name: 'Info',
  props: {
    email: String
  },
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      meu_link: 'http://www.google.com',
      texto_botao: 'Mostrar Email',
      technolgies: [
        'JavaScript',
        'Node.JS',
        'Sequelize ORM'
      ],
      tech_front: [
        {id: 1, language: 'Html'},
        {id: 2, language: 'CSS'},
        {id: 3, language: 'Vue'}
      ]
    }
  },
  components: {
    Picture
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
      if (!this.mostrar_email) {
          this.texto_botao = 'Mostrar email'
        } else {
          this.texto_botao = 'Esconder email'
      }
    }
  }
}
</script>