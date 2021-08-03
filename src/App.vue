<template>
  {{ count }}

  <button @click="count++">Incrementar</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      count: 0
    }
  },
  watch: {
    count(newValue, oldValue) {
      console.log(oldValue)
      console.log(newValue)
    }
  }
})
</script>
