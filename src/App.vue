<template>
  <p>{{ company }} é legal</p>

  <p v-text="company">é legal</p>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      company: 'Cataline'
    }
  }
})
</script>

<style scoped></style>
