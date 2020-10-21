<template>
  <div class="container py-4">
    <div class="text-center text-4xl">
      About Me
    </div>
    <hr class="border-t-4 border-red-600" />
    <div class="py-4 w-full sm:w-3/4 mx-auto">
      <div class="content">
        I started learning about web development while in college and pursuing
        my now completed bachelors degree in Information Technology. I took
        several database courses, and web development courses, along with
        general programming courses and picked up the basics of programming as
        well as scripting. I learned Java, Python, Linux, Unix, and Perl
        scripting.
      </div>

      <div class="content quote">
        Related Courses: Core Data Structures with Object Oriented Programming,
        Principles of Programming with Java, Shell and Script Programming with
        Unix, Foundations of Information Technology and Computer System
        Security, Web Programming, Information System Security, Web Design and
        Development
      </div>

      <div class="content">
        While in school, I got a job at Arizona State University as a help desk
        technician where I learned how to work as a team with other technicians
        and student workers. During this time, I also decided to pick up web
        development further on my own time outside of schooling and work. I took
        several Udemy courses about Html, CSS, and Javascript and began to put
        my skills together.
      </div>

      <div class="content">
        A couple of months later, I began to speak to our offices developer
        lead, where he led several other developers to create web applications
        for our department and showed him my interest in web development.
        Shortly after he spoke to our department manager and I got promoted to
        the development team building web applications for Arizona State
        University. During this time I picked up my first backend development
        skills and learned C# and ASP.NET.
      </div>

      <div class="content">
        After working in that department for almost 6 months, I was soon to be
        graduating and resigned from my position to pursue freelance development
        work. As a freelancer, I picked up Django and Django-Rest-Framework and
        frontend frameworks such as VueJS/NuxtJS. I have since built several
        full stack applications utilizing various frontends and backends and am
        confident I can pick up any backend and any frontend quickly.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "aboutindex",
  head() {
    return {
      title: "Michael James | About Me",
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: "description",
          name: "description",
          content:
            "Read about me, and my journey of how I became the web applications developer I am today."
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
.content {
  padding: 1rem 0;
}
.quote {
  border-left: 3px solid #e53e3e;
  padding-left: 1rem;
}
</style>
