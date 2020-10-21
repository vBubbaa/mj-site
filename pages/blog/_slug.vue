<template>
  <div class="container py-4">
    <div class="w-full">
      <postheader :post="post" />
    </div>
    <div class="w-full my-2">
      <nuxt-content :document="post" />
    </div>
  </div>
</template>

<script>
import postheader from "../../components/ui/postheader";

export default {
  name: "blogpost",
  components: {
    postheader
  },
  head() {
    return {
      title: `Blog | ${this.post.title}`,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content: `${this.post.description}`
        }
      ]
    };
  },
  async asyncData({ $content, params, error }) {
    let post;
    try {
      post = await $content("blog", params.slug).fetch();
    } catch (e) {
      error({ message: "Blog Post not found" });
    }

    return {
      post
    };
  }
};
</script>

<style></style>
