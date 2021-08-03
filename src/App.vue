<template>
  <a href="#interno" v-on:click="something">Link Interno </a>

  <a href="#interno" @click="something">Link Interno </a>

  <input type="text" name="" id="" @keyup.enter="something" />

  <input type="text" name="" id="" @keyup.k="something" />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  methods: {
    something() {
      console.log('Hello world')
    }
  }
})
</script>

<style scoped></style>
