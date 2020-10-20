<template>
  <div>
    <ul></ul>
  </div>
</template>

<script>
export default {
  head() {
    return {
      script: [
        { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" }
      ]
    };
  }
};
</script>

<style>
/* Bootstrap container */
.container {
  --bs-gutter-x: 1.5rem;
  width: 100%;
  padding-right: calc(var(--bs-gutter-x) / 2);
  padding-left: calc(var(--bs-gutter-x) / 2);
  margin-right: auto;
  margin-left: auto;
}

@media (min-width: 576px) {
  .container {
    max-width: 540px;
  }
}

@media (min-width: 768px) {
  .container {
    max-width: 720px;
  }
}

@media (min-width: 992px) {
  .container {
    max-width: 960px;
  }
}

@media (min-width: 1200px) {
  .container {
    max-width: 1140px;
  }
}

@media (min-width: 1400px) {
  .container {
    max-width: 1320px;
  }
}
</style>
