<template>
  <div>
    <div v-for="post of posts" :key="post.slug">
    <h2>{{ post.title }}</h2>
    <nuxt-content :document="post.body" />
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
  async asyncData({ $content }) {
    const posts = await $content("blog").fetch();

    return {
      posts,
    };
  },
}
</script>

<style>
</style>
