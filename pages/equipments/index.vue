<template>
  <main>
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <h1 class="title">Equipments</h1>
      <div v-for="post in posts" :key="post.slug">
        {{ post.category}}
      </div>
      <posts post-type="products" :amount="10" />
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let posts;
    try {
      posts = await $content("equipments").fetch();
    } catch (e) {
      error({ message: "Projects not found" });
    }
    return { posts };
  },
}
</script>
