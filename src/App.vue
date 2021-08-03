<template>
  <h1>{{ count }}</h1>

  <button @click="count++">Incrementar</button>
  <button @click="destroyComponent">Desmontar</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      count: 0
    }
  },
  beforeUnmount() {
    console.log('Antes de desmontar')
  },
  unmounted() {
    console.log('Depois de desmontar')
  },
  methods: {
    destroyComponent() {
      this.$.appContext.app.unmount()
    }
  }
})
</script>

<style scoped></style>
/* beforeCreated=> Created=> beforeMount=> mounted -> beforeUpdate -> updated =>
beforeUnmount => unmounted */
