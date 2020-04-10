<template>
    <div v-if="!seen">
        <p>
            Try to guess the 4-digit number.
        </p>
        <p>
            Digits cannot repeat.
        </p>
        <p>
            For every matching digit you get a cow or a bull. <br>
            Bulls are correct digits and in the correct position, and cows are correct digits but not in the right
            position.
        </p>
        <button class="btn" @click="markSeen()">
            Got it ;)
        </button>
    </div>
</template>

<style scoped>
    .btn {
        color: #c38d9d;
        font-size: 1.1em;
        border-radius: 3px;
        background-color: bluegray;
        font-weight:bold;
    }

</style>

<script>
export default {
  data () {
    return {
        seen: !!localStorage.getItem("seen")
    }
  },
  methods: {
    markSeen: function () {
        localStorage.setItem("seen", true);
        this.seen = true;
    }
  }
}

</script>