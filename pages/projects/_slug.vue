<template>
  <div class="pb-6">
    <img
      :src="project.headerimage"
      :alt="project.title + '\'s header image.'"
      class="w-full h-64 object-cover mb-4"
    />
    <div class="container">
      <div class="text-center text-3xl font-bold">
        {{ project.title }}
      </div>
      <div class="text-center w-full sm:w-3/4 mx-auto">
        <i>{{ project.description }}</i>
      </div>
      <div class="flex flex-col sm:flex-row items-center justify-around my-2">
        <div v-if="project.code">
          <a target="_blank" :href="project.code"
            ><cbutton text="View Code"
          /></a>
        </div>
        <div v-if="project.frontendcode">
          <a target="_blank" :href="project.frontendcode"
            ><cbutton text="Frontend Code"
          /></a>
        </div>
        <div v-if="project.backendcode">
          <a target="_blank" :href="project.backendcode"
            ><cbutton text="Backend Code"
          /></a>
        </div>
        <div v-if="project.livesite">
          <a target="_blank" :href="project.livesite"
            ><cbutton text="View Site"
          /></a>
        </div>
      </div>
      <hr class="border-t-2 border-red-600 my-2" />
      <div>
        <nuxt-content :document="project" />
      </div>
    </div>
  </div>
</template>

<script>
import cbutton from "../../components/ui/cbutton";

export default {
  name: "projectdetail",
  components: {
    cbutton
  },
  head() {
    return {
      title: `Project | ${this.project.title}`,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content: `${this.project.description}`
        }
      ]
    };
  },
  async asyncData({ $content, params, error }) {
    let project;
    try {
      project = await $content("projects", params.slug).fetch();
    } catch (e) {
      error({ message: "Project not found" });
    }

    return {
      project
    };
  }
};
</script>

<style lang="scss" scoped></style>
