<template>
  <div>
    <h1>How was your day ?</h1>
    <input v-model="yourAnswer" type="text" placeholder="enter your answer" />
    <button @click="answer">submit</button>
  </div>
</template>
<script>
export default {
  data () {
    return {
      yourAnswer: 'good'
    }
  },
  methods: {
    answer () {
      this.$router.push(`/regards/${this.yourAnswer}`)
    }
  }
}
</script>
