---
title: Portfolio Website
date: 2020-10-21T21:55:39.828Z
description: My personal website showcasing projects, a web-development related
  blog, an about me page, and my online resume.
code: https://github.com/vBubbaa/mj-site
livesite: https://vbubbaa.dev/
headerimage: /img/mj-site-header.png
---

# My Personal Website/Blog

My personal website utilizes NuxtJS and Netlify CMS to create a static-generated website including collections such as projects and blog posts, as well as an online resume and an about page.

The website is deployed to Netlify with a custom domain from Google Domains. Netlify allows me to include a .yml file for continuous deployments on main branch code pushes.

Netlify CMS allows for creating collections with various fields and is stored in markdown format. Projects and Blog posts use the CMS and generate markdown files which are fed into the Nuxt-Content module to display markdown content and statically generate them. Nuxt-Content also allows for in-browser editing making it very easy to create projects and blog posts.

All styling is created with TailwindCSS.

## Technologies

- NuxtJS
- Nuxt-Content
- Netlify CMS
- TailwindCSS
- Fontawesome
