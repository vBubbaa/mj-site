<template>
  <div class="w-full container py-4">
    <div class="text-center text-4xl">Hi, I'm Michael James.</div>
    <div class="text-center text-xl w-full mx-auto sm:w-3/4">
      I am a passionate full-stack web applications developer with a history of
      developing rich and dynamic web applications. I have a degree in
      Information Technology from Arizona State University and have been
      building web applications for three years.
    </div>
    <div class="mx-auto py-4">
      <img
        src="~/assets/images/me.jpg"
        alt="Michael James' profile picture"
        class=" rounded-full w-40 h-40 object-cover mx-auto"
      />
    </div>
    <div></div>
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
