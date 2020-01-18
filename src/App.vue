<template>
  <div id="app">
    <MainPage/>
    <!--
    MainPage
      Introduction
      list of PlayerArea
          Goal
            btnUnlock
            Input (faded)
            btnReveal
          btnMakeIntoAI
          list of Guess
              value
              result
                  bulls
                  cows
          guess input  + submit btn
          btnHelpFromAi
          btnRemovePlayer
      btnAddPlayer

    -->
  </div>
</template>

<script>
import MainPage from './views/MainPage.vue'

export default {
  name: 'app',
  components: {
    MainPage
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
