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
    </div>

    <div class="content">
      <div class="font-bold">Professional Profile</div>
      <div>
        Passionate full-stack web applications developer with a history of
        developing rich and dynamic web applications. Experience with building
        backends and restful APIs with technologies including Django and Django
        Rest Framework as well as building frontend applications using VueJS and
        NuxtJS.
      </div>
    </div>

    <div class="content">
      <div class="font-bold">Education</div>
      <div>
        <div>Information Technology (B.S) 2020</div>
        <div>Arizona State University</div>
        <div>
          <b>Relevant Courses</b>: Core Data Structures with Object Oriented
          Programming, Principles of Programming with Java, Shell and Script
          Programming with Unix, Foundations of Information Technology and
          Computer System Security, Web Programming, Information System
          Security, Web Design and Development
        </div>
      </div>
    </div>

    <div class="content">
      <div class="font-bold">Skills</div>
      <div>
        <ul>
          <li>
            Programming and Scripting Languages: Python, Javascript, C#, HTML5,
            CSS3
          </li>
          <li>
            Backend Technologies: Django, Django Rest Framework, ASP.NET, SQLite
          </li>
          <li>
            Frontend Technologies: VueJS, VueX, NuxtJS, Vuetify, Bootstrap,
            JQuery
          </li>
          <li>Systems: Windows (XP, 7, 8, 10), Linux, MAC OS</li>
          <li>Workflows: Jira / SCRUM / Trello</li>
          <li>
            Other: Adobe Photoshop, Microsoft Suite, Active Directory, SCCM,
            JAMF, Git, Github
          </li>
        </ul>
      </div>
    </div>

    <div class="content">
      <div class="py-2">
        <div class="font-bold">Work Experience</div>
        <div>
          <div>
            <i><u>Freelance Full Stack Web Developer | 3/19 – Current</u></i>
          </div>
          <div>
            <ul>
              <li>
                Mainly developing one large scale project which interacts with
                the popular gaming platform Steam. Utilizes Django Rest
                Framework backend with a NuxtJS frontend to build a dynamic and
                rich website that tracks steam app information, and lets users
                compare app libraries with friends.
              </li>
              <li>SEO Audits and fixes for small websites</li>
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
          After working as a help desk technician, I was promoted to a full
          stack web developer in the offices’ development team where I developed
          and maintained several websites for Arizona State University.
          <ul>
            <li>
              Developed and managed several Arizona State University websites
              using ASP.NET, HTML, CSS, Javascript
            </li>
            <li>
              Connected websites with the schools Active Directory using LDAP
            </li>
            <li>Updated and maintained the IT departments ticketing system</li>
          </ul>
        </div>
        <div>
          <div class="font-bold py-2">Notable Projects:</div>
          <div>
            <ul>
              <li>Active Directory integration with LDAP</li>
              <li>
                <a
                  href="https://herbergerinstitute.asu.edu/research-and-initiatives/counteract"
                  target="_blank"
                  >Counteract</a
                >: A project allowing students to submit actions of
                counteracting acts of sexual violence via image or video
                uploads. Includes image and video processing, profile
                customization, and backend administrative options for faculty
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "cvindex"
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
</style>
