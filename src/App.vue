<template>
  <h1>{{ message }}</h1>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      message: 'Hello world'
    }
  },
  beforeCreate() {
    console.log('Antes da criação')
  },
  created() {
    console.log('Depois da criação')
  }
})
</script>

<style scoped></style>
/* beforeCreated=> Created=> beforeMount=> mounted -> beforeUpdate -> updated =>
beforeUnmount => unmounted */
