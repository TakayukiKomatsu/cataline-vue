<template>
  <h1>{{ person }}</h1>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      person: {} as Person
    }
  }
})
</script>
