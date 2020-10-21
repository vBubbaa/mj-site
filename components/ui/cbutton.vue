<template>
  <button
    class="bg-red-500 p-2 rounded my-2 bg-transparent hover:bg-red-600 text-white font-bold"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "cbutton",
  props: {
    text: String
  }
};
</script>

<style lang="scss" scoped></style>
