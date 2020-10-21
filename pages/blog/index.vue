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
  head() {
    return {
      title: "Michael James | Blog",
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content:
            "View Michael James' blog regarding all thing web development related"
        }
      ]
    };
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
