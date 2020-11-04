<template>
  <div class="container py-4">
    <div class="text-center text-4xl">
      Resume
    </div>
    <hr class="border-t-4 border-red-600" />

    <div class="content">
      <div>Michael James</div>
      <div>
        <a
          target="_blank"
          href="https://www.linkedin.com/in/michael-james-60b81216b/"
          >LinkedIn</a
        >
      </div>
      <div><a target="_blank" href="https://github.com/vBubbaa">Github</a></div>
      <div>
        *Willing to relocate anywhere in the US
      </div>
    </div>

    <div class="content">
      <div class="font-bold">Skills</div>
      <div>
        <ul>
          <li>
            Python, JavaScript, C#, HTML, CSS, JQuery, Ajax, VueJS, NuxtJS,
            Bootstrap, Vuetify, Django, Django Rest Framework, Django Rest
            Authentication, ASP.NET, SQL, Jira / Scrum, JWT Authentication,
            Photoshop
          </li>
        </ul>
      </div>
    </div>

    <div class="content">
      <div class="font-bold">Education</div>
      <div>
        <div>
          <i
            ><u
              >Information Technology (B.S) | Arizona State University | 2020</u
            ></i
          >
        </div>
        <div>
          <ul>
            <li>Emphasis in Computer Networking and Database Systems</li>
            <li>Web Development courses using HTML, CSS, and Javascript</li>
            <li>
              Courses relating to cyber-security and Linux/Unix administration
            </li>
            <li>
              Capstone project allowing users to use and Android phone to
              control a mouse on screen controlled only with facial movements
              including on screen clicking functionality
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="content noborder">
      <div class="py-2">
        <div class="font-bold">Work Experience</div>
        <div>
          <div>
            <i><u>Full Stack Web Developer | 3/19 – Current | Freelance</u></i>
          </div>
          <div>
            <ul>
              <li>
                Built and deployed Django and Django Rest Framework backends
              </li>
              <li>
                Built and deployed dynamic and mobile responsive front-end web
                applications with VueJS
              </li>
              <li>Utilized NuxtJS for server-side rendering</li>
              <li>
                Implemented the Vuetify material UI library to build out elegant
                front-end web applications
              </li>
              <li>
                Used OpenID to authenticate using the Steam platform using
                Django Rest Authentication
              </li>
            </ul>
          </div>
        </div>
      </div>

      <div class="py-2">
        <div>
          <i
            ><u
              >Full Stack Web Developer | Arizona State University | 8/18 – 3/19
            </u></i
          >
        </div>
        <div>
          <ul>
            <li>
              Developed and managed several Arizona State University Herberger
              Institute websites
            </li>
            <li>Worked with the ASP.NET backend to build views and models</li>
            <li>
              Used HTML, CSS, Javascript, and JQuery to build the front-end of
              the webpages
            </li>
            <li>
              Connected ASP.NET with active directory using the LDAP protocol
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "cvindex",
  head() {
    return {
      title: "Michael James | Resume",
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content:
            "Michael James' resume showcasing work experience, skills, and education."
        }
      ]
    };
  }
};
</script>

<style scoped>
a {
  color: #e53e3e;
}
a:hover {
  font-weight: bold;
}
li {
  list-style-type: circle;
  margin-left: 1.5rem;
  padding-left: 0.5rem;
}
.content {
  border-bottom: 1px solid #e53e3e;
  padding: 1rem 0;
}

.noborder {
  border-bottom: none;
}
</style>
