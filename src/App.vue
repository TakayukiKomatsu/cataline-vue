<template>
  <h1>{{ fullName }}</h1>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      name: 'Takayuki',
      lastName: 'Komatsu'
    }
  },
  computed: {
    fullName(): string {
      return `${this.name} ${this.lastName}`
    }
  }
})
</script>
