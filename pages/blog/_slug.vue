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

<style>
.nuxt-content h1 {
  font-weight: bold;
  font-size: 28px;
}
.nuxt-content h2 {
  font-weight: bold;
  font-size: 24px;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}
.nuxt-content p {
  margin-bottom: 20px;
}
.nuxt-content pre {
  background: #d7d7d7;
}
.nuxt-content a {
  color: #e53e3e;
}
.nuxt-content a:hover {
  border-bottom: 1px solid #e53e3e;
}
.nuxt-content table {
  margin: auto;
}
.nuxt-content td,
.nuxt-content th {
  border: 1px solid black;
}
.nuxt-content blockquote {
  border-left: 3px solid #e53e3e;
  padding-left: 2rem;
  color: gray;
}
.nuxt-content li {
  margin-left: 1.5rem;
  padding-left: 0.5rem;
  list-style-type: square;
}
</style>
