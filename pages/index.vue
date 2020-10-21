<template>
  <div class="flex h-screen justify-center items-center container py-4">
    <div class="">
      <div class="text-center text-4xl">Hi, I'm Michael James.</div>
      <div class="text-center text-xl w-full mx-auto sm:w-3/4">
        I am a passionate full-stack web applications developer with a history
        of developing rich and dynamic web applications. I have a degree in
        Information Technology from Arizona State University and have been
        coding and creating web applications for several years.
      </div>
      <div class="mx-auto py-4">
        <img
          src="~/assets/images/me.jpg"
          alt="Michael James' profile picture"
          class=" rounded-full w-40 h-40 object-cover mx-auto"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      script: [
        { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" }
      ],
      title: `Michael James | Web Applications Developer`,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content:
            "I am a passionate full-stack web applications developer with a history of developing rich and dynamic web applications."
        }
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

/* Netlify content styling for markdown */
.nuxt-content h1 {
  font-weight: bold;
  font-size: 28px;
}
.nuxt-content h2 {
  font-weight: bold;
  font-size: 24px;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}
.nuxt-content p {
  margin-bottom: 20px;
}
.nuxt-content pre {
  background: #d7d7d7;
}
.nuxt-content a {
  color: #e53e3e;
}
.nuxt-content a:hover {
  border-bottom: 1px solid #e53e3e;
}
.nuxt-content table {
  margin: auto;
}
.nuxt-content td,
.nuxt-content th {
  border: 1px solid black;
}
.nuxt-content blockquote {
  border-left: 3px solid #e53e3e;
  padding-left: 2rem;
  color: gray;
}
.nuxt-content li {
  margin-left: 1.5rem;
  padding-left: 0.5rem;
  list-style-type: square;
}
</style>
