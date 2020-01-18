<template>
    <div class="playerArea">
        <p>{{name}}</p>

        <input type="text" />
        <button class="btn">guess!</button>
    </div>
</template>

<script>
export default {
    props: ["name"],
    data() { return {
        guesses: []
    }}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.playerArea {
    display: inline-block;
}
</style>
