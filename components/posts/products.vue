<template>
  <ul>
    <li v-for="product in products" :key="product.slug">
      <nuxt-link :to="`/${type}/${product.slug}`">
        <img :src="product.cover" class="w-auto-full" />
        <h3>{{product.title}}</h3>
      </nuxt-link>
    </li>
  </ul>
</template>

<script>
export default {
  name: "products",
  props: {
    products: {
      required: true,
      type: Array
    },
    type: {
      type: String,
      default: 'products'
    }
  }
}
</script>

<style scoped>

</style>