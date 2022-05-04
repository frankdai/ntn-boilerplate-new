<template>
  <main>
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <h1 class="title">Auto Parts</h1>
      <products :products="posts" />
    </section>
  </main>
</template>

<script>
import products from "~/components/posts/products";
export default {
  async asyncData({ $content, error }) {
    let posts;
    try {
      posts = await $content("products").where({ category: { $eq: 'auto_parts' } }).fetch();
    } catch (e) {
      error({ message: "Projects not found" });
    }
    return { posts };
  },
  components: {
    products
  }
}
</script>
