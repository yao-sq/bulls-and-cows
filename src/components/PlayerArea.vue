<template>
    <div class="playerArea">
        <div>
            <p>{{goal}}</p>
            <input v-model="goal" placeholder="1234">
            <button class="btn" @click="markHide">
                confirm!
            </button>
        </div>


        <div>
            <p>{{name}}</p>
            <input v-model="guess" placeholder="1234">
            <button class="btn" @click="checkIfFourDigits()">
                guess!
            </button>
        </div>

    </div>


</template>

<script>
export default {
    props: ["name"],

    data() { return {
        guesses: [
            {value: "1234", result: {bulls: 1, cows: 2}},
            {value: "5678", result: {bulls: 0, cows: 1}}
        ]
    }},

    methods: {
      checkIfFourDigits: function () {
        if (!((this.guess.length==4) && (!isNaN(this.guess)))) {
          console.log("output a 4-digit number")
        }
      },

      getBullsCows: function () {

      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.playerArea {
    display: inline-block;
}
</style>
