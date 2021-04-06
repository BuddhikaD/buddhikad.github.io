<template>
  <div class="about page  animate__animated animate__fadeIn">
    <h2>Recent Project</h2>
    <div class="container">
      <div class="row" v-for="(project, index) in projects" :key="index">
        <div class="col-md-5">
          <img
            :src="project.image_cover"
            :alt="project.title"
            class="project-cover"
          />
        </div>
        <div class="col-md-5">
          <h2 class="mt-3" style="text-align: left;">
            {{ project.title }}
            <hr class="dope"/>
          </h2>
          <b-card class="mt-3 mb-3 text-left text-dark">
            <p>{{ project.description }}</p>
            <b-link :href="project.link"
            >Check it out!
              <LinkIcon style="color: #000;"
              />
            </b-link>
            <hr/>
            <b-link :href="project.github_url"
            >View source code
              <GithubIcon style="color: #000;"
              />
            </b-link>
          </b-card>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import LinkIcon from "vue-ionicons/dist/md-link.vue";
import GithubIcon from "vue-ionicons/dist/logo-github.vue";

export default {
  components: {
    GithubIcon,
    LinkIcon
  },
  data() {
    return {
      projects: [
        {
          title: "Event-Booking App",
          tag: "Android Event-Booking App",
          description:
            "Our product is an Android Event-booking App. It is an entertainment-related one. Admin can create events, and users can book tickets for their exciting events",
          image_cover: require("@/assets/app.jpg"),
          github_url: "https://github.com/Yasiruofficial/let_me_out_app",
          link: "https://github.com/Yasiruofficial/let_me_out_app"
        },
        {
          title: "Volunteer Onboard Site",
          tag: "Organization volunteer site",
          description:
            "Project profile for volunteers,Free and Open Source Project developed by Satriaana Volunteers",
          image_cover: require("@/assets/volunteer.jpg"),
          github_url: "https://github.com/Satriaana/cb-vol-site",
          link: "https://volunteer.satriaana.org/"
        },
        {
          title: "Organization Website",
          tag: "Satriaana website",
          description:
            "This Project will be the official website for Satriaana Organization which includes about the organization and the forum.",
          image_cover: require("@/assets/satriaana.jpg"),
          github_url: "https://github.com/Satriaana/Satriaana-Web-Site",
          link: "https://satriaana.org"
        }
      ],
    };
  },
  methods: {
    isEven(n) {
      if (n % 2 == 0) {
        return true;
      } else {
        return false;
      }
    }
  },
  head: {
    title: "Recent Projects 💻 - Buddhika Dananjaya",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "View all the recents open-sourced projects built with ♥ by Buddhika Dananjaya, open-sourced means this project source code are publicly available for everyone to use or modify."
      },
      {
        hid: "og:title",
        name: "og:title",
        content: "Recent Projects 💻 - Buddhika Dananjaya"
      },
      {
        property: "og:description",
        content:
          "View all the recents open-sourced projects built with ♥ by Buddhika Dananjaya, open-sourced means this project source code are publicly available for everyone to use or modify., open-sourced means this project source code are publicly available for everyone to use or modify."
      },
      {
        hid: "og:image",
        name: "og:image",
        content: require("@/assets/man-computer.png")
      }
    ]
  }
};
</script>
<style scoped>
.row {
  margin-top: 70px;
}

.project-cover {
  width: inherit;
  border-radius: 3px;
}

hr.dope {
  border: 0;
  width: 90px;
  border-top: 2px solid #dc3545;
  text-align: left;
  margin: initial;
  margin-top: 7px;
  margin-left: 5px;
}
</style>
