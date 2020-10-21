<template>
  <div class="container py-4">
    <div class="text-center text-4xl">
      Projects
    </div>
    <hr class="border-t-4 border-red-600" />
    <div class="py-4">
      <div v-for="project in projects" :key="project.slug">
        <projectcard :project="project" />
      </div>
    </div>
  </div>
</template>

<script>
import projectcard from "../../components/ui/projectcard";

export default {
  name: "projectindex",
  components: {
    projectcard
  },
  async asyncData({ $content }) {
    const projects = await $content("projects").fetch();

    return {
      projects
    };
  }
};
</script>

<style lang="scss" scoped></style>
