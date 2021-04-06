<template>
  <div class="container animate__animated animate__fadeIn">
    <div class="row">
      <div class="col-md-6">
        <div class="about">
          <h1 class="line-after">About Me</h1>
          <h4 class="mt-4">Hey 👋</h4>
          <p>
            My name is Buddhika, And I am FOSS and Linux Enthusiast ,A knowledge
            seeker and a hard worker. Friendly helpful and polite, have a good
            sense of humor.Able to work in busy environments and also within a
            team setting. Creative problem solver with strong interpersonal
            skills. Good in organizing work and meeting deadlines. Currently
            Study BSc in Management Information Systems (Special) at NSBM Green
            University, Sri Lanka.<br><br>
             I love sharing knowledge and being a tech
            speaker at different programs. I mainly focus on channeling my
            skills into open source projects and sharing it with the community
            by mentoring, running workshops, writing blogs to help make the
            world a better and more developed place.<br><br> 
            My fields of interest are
            web development , Cloud & mobile application development, I have
            special interests in volunteering in Open Source Communities and
            writing articles to FOSS NSBM Community, Medium, FOSS Sri Lanka
          </p>
          <h4 class="mt-5">Tech Stacks</h4>
          <p>Below are some of the technologies I use daily:</p>
          <div class="row animate__animated animate__fadeInUp">
            <div class="col">
              <ul style="list-style-type: circle;">
                <li>HTML & CSS</li>
                <li>Python</li>
                <li>Bash</li>
              </ul>
            </div>
            <div class="col">
              <ul style="list-style-type: circle;">
                <li>JavaScript</li>
                <li>Vue</li>
                <li>Flutter</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <img
          src="@/assets/working.png"
          alt="About Illustration"
          class="abt-img"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      startYear: 2017,
      currYear: new Date().getFullYear(),
      stacks: [
        {
          language: "HTML",
          experience: "3+ Years",
          variant: "secondary",
          breif: "lorem..."
        },
        {
          language: "CSS",
          experience: "3+ Years",
          variant: "primary",
          breif: "lorem..."
        },
        {
          language: "Javascript",
          experience: "2+ Years",
          variant: "warning",
          breif: "lorem..."
        },
        {
          language: "VUE",
          experience: "1 Years",
          variant: "success",
          breif: "lorem..."
        },
        {
          language: "Python",
          experience: "2 Years",
          variant: "dark",
          breif: "lorem..."
        }
      ]
    };
  },
  head: {
    title: "About 🕵️‍♂️ - Buddhika",
    meta: [
      {
        hid: "description",
        name: "description",
        // currYear - startYear
        content: `Hey there 👋 My name is Buddhika Dananjaya, And I am FOSS and Linux Enthusiast ,Currently Study BSc in Management Information Systems (Special) at NSBM Green University, Sri Lanka`
      }
    ]
  }
};
</script>
<style scoped>
.container {
  margin-top: 140px;
  text-align: left;
}

.line-after {
  overflow: hidden;
}

.line-after::after {
  content: "";
  display: inline-block;
  height: 0.5em;
  vertical-align: bottom;
  width: 100%;
  margin-right: -100%;
  margin-left: 10px;
  border-top: 2px solid rgb(211, 46, 46);
}

.abt-img {
  width: inherit;
  height: inherit;
  border-radius: 5px;
}

/* .abt-img:hover {
  animation: swing;
  animation-duration: 2s;
} */
</style>
