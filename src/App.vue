<template>
  <h1>{{ count }}</h1>

  <button @click="increment">Incrementar</button>
  <button @click="decrease">Diminuir</button>
  <button @click="reset">Resetar</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++
    },
    decrease() {
      this.count--
    },
    reset() {
      this.count = 0
    }
  }
})
</script>
