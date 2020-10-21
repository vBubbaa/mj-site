<template>
  <div class="container py-4">
    <div class="text-center text-4xl">
      Projects
    </div>
    <hr class="border-t-4 border-red-600" />
    <div v-for="project in projects" :key="project.slug">
      {{ project }}
    </div>
  </div>
</template>

<script>
export default {
  name: "projectindex",
  async asyncData({ $content }) {
    const projects = await $content("projects").fetch();

    return {
      projects
    };
  }
};
</script>

<style lang="scss" scoped></style>
