<template>
  <h1>Meu formulário</h1>
  <form action="">
    <InputText />
    <InputText />
    <InputSubmit />
  </form>
</template>

<script>
import InputText from './form/InpuText.vue'
import InputSubmit from './form/InputSubmit.vue'

export default {
  components: {
    InputText,
    InputSubmit
  }
}
</script>