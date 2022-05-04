<template>
  <ul>
    <li v-for="product in products" :key="product.slug">{{product.title}}</li>
  </ul>
</template>

<script>
export default {
  name: "products",
  props: {
    products: {
      required: true,
      type: Array
    }
  }
}
</script>

<style scoped>

</style>