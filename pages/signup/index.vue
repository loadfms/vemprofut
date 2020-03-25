<template>
  <div class="signup-container">
    <Question text="Saudaçoes! Conte-me um pouco sobre voce..." helptext="Precisamos de alguns dados para voce se cadastrar, mas e rapidinho!" />

    <div class="inputs">
      <Textbox v-if="questions[step] !== undefined" :placeholder="questions[step]" :input-data.sync=" actualAnswer" />
    </div>

    <div class="buttons">
      <Actionbutton v-if="questions[step] !== undefined" text="continuar" @clicked="handleClick" />
      <Button v-if="questions[step] === undefined" text="Montar o time" />
    </div>
  </div>
</template>

<script>
import Question from '~/components/Question/'
import Textbox from '~/components/Textbox'
import Actionbutton from '~/components/Actionbutton'
import Button from '~/components/Button'

export default {
  components: {
    Question,
    Textbox,
    Actionbutton,
    Button
  },
  data () {
    return {
      step: 0,
      questions: [
        'Qual seu nome?',
        'Qual seu email?'
      ],
      actualAnswer: '',
      answers: []
    }
  },
  methods: {
    handleClick () {
      this.step++
      this.answers.push(this.actualAnswer)
      this.actualAnswer = ''
    }
  }
}
</script>

<style lang="scss" src="./index.scss">
</style>
