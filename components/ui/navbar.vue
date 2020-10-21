<template>
  <nav
    class="flex items-center justify-between flex-wrap bg-transparent p-6 bg-red-600"
  >
    <div class="flex items-center flex-no-shrink text-white mr-6">
      <nuxt-link to="/">
        <span class="font-semibold text-xl tracking-tight">Michael James</span>
      </nuxt-link>
    </div>
    <div class="block sm:hidden">
      <button
        @click="toggle"
        class="flex items-center px-3 py-2 border rounded text-white border-teal-light hover:text-gray-400 hover:border-white"
      >
        <svg
          class="fill-current h-3 w-3"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
      </button>
    </div>
    <div
      :class="open ? 'block' : 'hidden'"
      class="w-full flex-grow sm:flex sm:items-center sm:w-auto"
    >
      <div class="text-sm sm:flex-grow">
        <nuxt-link
          :to="{ name: 'projects' }"
          class="no-underline block mt-4 sm:inline-block sm:mt-0 text-white hover:text-gray-400 mr-4"
        >
          Projects
        </nuxt-link>
        <nuxt-link
          :to="{ name: 'cv' }"
          class="no-underline block mt-4 sm:inline-block sm:mt-0 text-white hover:text-gray-400 mr-4"
        >
          Resume
        </nuxt-link>
        <nuxt-link
          :to="{ name: 'blog' }"
          class="no-underline block mt-4 sm:inline-block sm:mt-0 text-white hover:text-gray-400 mr-4"
        >
          Blog
        </nuxt-link>
        <nuxt-link
          :to="{ name: 'about' }"
          class="no-underline block mt-4 sm:inline-block sm:mt-0 text-white hover:text-gray-400"
        >
          About
        </nuxt-link>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "navbar",

  data: function() {
    return {
      open: false
    };
  },

  methods: {
    toggle() {
      this.open = !this.open;
    }
  }
};
</script>

<style lang="scss" scoped></style>
