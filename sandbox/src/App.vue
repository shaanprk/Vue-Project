<script>
  export default {
    data() {
      return {
        message: 'It works.',
        count: 0
      }
    },
    methods: {
      incrementCount() {
        this.count++
      }
    }
  }
</script>

<template>
  <h1>Counter</h1>
    <p>{{ count }}</p>
    <button v-on:click="incrementCount">Increment Count</button>
    <hr/>
</template>