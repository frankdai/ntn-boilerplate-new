<template>
  <main>
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <h1 class="title">Production Equipment</h1>
      <products :products="posts" type="equipments" />
    </section>
  </main>
</template>

<script>
import products from "~/components/posts/products";
export default {
  async asyncData({ $content, error }) {
    let posts;
    try {
      posts = await $content("equipments").where({ category: { $eq: 'production_equipment' } }).fetch();
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
