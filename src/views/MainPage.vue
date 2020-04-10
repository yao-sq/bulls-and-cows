<template>
    <div>
        <Introduction class="intro"/>
        <PlayerArea class="player" v-for="player in players" :name="player.name" :key="player.name" />
    </div>
</template>


<script>
import Introduction from '../components/Introduction.vue'
import PlayerArea from '../components/PlayerArea.vue'

export default {
 data () { return {
    players: [
      { name: "Player 1" },
      { name: "Player 2" }
    ]
  }},

    components: {
        Introduction,
        PlayerArea
    }
}

</script>

<style scoped>
    .intro {
        text-align: justify;
    }
    .player {
        margin-left: 5em;
    }

</style>