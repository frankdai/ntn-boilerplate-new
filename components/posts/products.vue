<template>
  <ul>
    <li v-for="product in products" :key="product.slug" class="flex flex-wrap py-4">
      <nuxt-link :to="`/${type}/${product.slug}`" class="w-1/4 border p-2 rounded">
        <img :src="product.cover" class="w-auto-full" />
        <h5 class="text-center">{{product.title}}</h5>
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