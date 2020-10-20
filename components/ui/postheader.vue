<template>
  <div class="w-full my-2">
    <div class="text-4xl">
      {{ post.title }}
    </div>
    <div class="text-xl">{{ date(post.createdAt) }}</div>
    <div class="text-xl">
      Michael James
    </div>
    <hr class="border-t-4 border-red-600 my-2" />
    <div class="text-lg py-2 my-4">
      <div>Brief</div>
      <i>{{ post.description }}</i>
    </div>
  </div>
</template>

<script>
export default {
  name: "postheader",
  props: {
    post: Object
  },
  methods: {
    date: function(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    }
  }
};
</script>

<style lang="scss" scoped></style>
