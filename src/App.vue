<template>
  <a :href="product.url" :class="productClass">{{ product.name }}</a>

  OR

  <a v-bind:href="product.url" v-bind:class="productClass">{{
    product.name
  }}</a>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      product: {
        name: 'Camisa',
        url: 'http://loja.com/produtos/12345',
        stock: true
      }
    }
  },
  computed: {
    productClass(): string {
      return this.product.stock ? 'success' : 'danger'
    }
  }
})
</script>

<style scoped>
.danger {
  color: red;
}
.success {
  color: green;
}
</style>
