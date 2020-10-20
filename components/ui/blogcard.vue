<template>
  <div class="w-full p-4 m-4 border-b-4 border-red-600">
    <div class="text-3xl py-1">{{ blog.title }}</div>
    <div class="py-1">Created: {{ blog.createdAt }}</div>
    <div class="py-1">{{ blog.description }}</div>

    <nuxt-link
      class="text-red-600 hover:font-bold"
      :to="{ name: 'blog-slug', params: { slug: blog.slug } }"
      >Read More</nuxt-link
    >
  </div>
</template>

<script>
export default {
  name: "blogcard",
  props: {
    blog: Object
  }
};
</script>

<style lang="scss" scoped></style>
