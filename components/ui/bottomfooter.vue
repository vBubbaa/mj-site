<template>
  <div>
    <footer>
      <div class="flex justify-center bg-red-600 p-4">
        <a
          target="_blank"
          href="https://www.linkedin.com/in/michael-james-60b81216b/"
        >
          <font-awesome-icon
            :icon="['fab', 'linkedin']"
            size="2x"
            class="mx-2 text-white hover:text-gray-400"
          />
        </a>
        <a target="_blank" href="https://github.com/vBubbaa">
          <font-awesome-icon
            :icon="['fab', 'github']"
            size="2x"
            class="mx-2 text-white hover:text-gray-400"
          />
        </a>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "bottomfooter"
};
</script>

<style lang="scss" scoped></style>
