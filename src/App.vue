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
  beforeMount() {
    console.log(this.$el)
  },
  mounted() {
    console.log(this.$el)
  }
})
</script>

<style scoped></style>
/* beforeCreated=> Created=> beforeMount=> mounted -> beforeUpdate -> updated =>
beforeUnmount => unmounted */
