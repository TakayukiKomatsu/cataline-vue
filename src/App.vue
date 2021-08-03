<template>
  <h1>{{ count }}</h1>
  <button @click="count++"></button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      count: 0
    }
  },
  beforeUpdate() {
    console.log('Antes da atualização')
  },
  updated() {
    console.log('Depois da atualização')
    if (this.count == 5) this.count = 6
  }
})
</script>

<style scoped></style>
/* beforeCreated=> Created=> beforeMount=> mounted -> beforeUpdate -> updated =>
beforeUnmount => unmounted */
