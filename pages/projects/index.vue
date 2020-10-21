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
  head() {
    return {
      title: "Michael James | Projects",
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content: "View Michael James' projects."
        }
      ]
    };
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
