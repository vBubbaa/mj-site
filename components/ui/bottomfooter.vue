<template>
  <div>
    <footer>
      <div class="flex justify-center bg-red-600 p-4">
        <font-awesome-icon
          :icon="['fab', 'linkedin']"
          size="2x"
          class="mx-2 text-white hover:text-gray-400"
        />
        <font-awesome-icon
          :icon="['fab', 'github']"
          size="2x"
          class="mx-2 text-white hover:text-gray-400"
        />
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
