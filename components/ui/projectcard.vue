<template>
  <div>
    <div class="text-4xl text-red-400">{{ project.title }}</div>
    <div class="text-xl">
      <i>{{ project.description }}</i>
    </div>
    <nuxt-link :to="{ name: 'projects-slug', params: { slug: project.slug } }">
      <cbutton text="View Project" />
    </nuxt-link>
  </div>
</template>

<script>
import cbutton from "../../components/ui/cbutton";

export default {
  name: "projectcard",
  props: {
    project: Object
  },
  components: {
    cbutton
  }
};
</script>

<style scoped></style>
