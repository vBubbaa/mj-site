<template>
  <div class="container py-4">
    <div class="text-center text-4xl">
      Blog Posts
    </div>
    <div v-for="post of posts" :key="post.slug" class="w-full">
      <blogcard :blog="post" />
    </div>
  </div>
</template>

<script>
import blogcard from "../../components/ui/blogcard";
export default {
  name: "blogindex",
  components: {
    blogcard
  },
  async asyncData({ $content }) {
    const posts = await $content("blog").fetch();

    return {
      posts
    };
  }
};
</script>

<style scoped></style>
