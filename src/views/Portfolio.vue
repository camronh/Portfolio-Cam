<template>
  <div>
    <v-app-bar flat color="transparent">
      <v-toolbar-title>
        Portfolio
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <AvatarMenu />
    </v-app-bar>
    <br />
    <br />
    <br />
    <br />
    <br />
    <v-container fluid pa-0>
      <v-row align="center" justify="center" dense>
        <v-col cols="12" lg="6" md="6">
          <v-card color="transparent">
            <v-card-title>
              <h2>
                My Work
              </h2>
            </v-card-title>
            <v-card-subtitle>
              Here are some of the projects that I have worked on
            </v-card-subtitle>

            <v-card-text>
              <span class="subheading">Select Stack</span>

              <v-chip-group
                v-model="selectedStack"
                active-class="primary--text"
                multiple
              >
                <v-chip v-for="skill of skills" :key="skill" outlined>
                  {{ skill }}
                </v-chip>
              </v-chip-group>
            </v-card-text>
            <v-divider></v-divider>
            <v-container fluid>
              <v-row dense>
                <v-col
                  v-for="project in filteredProjects"
                  :key="project.title"
                  :cols="project.flex"
                >
                  <v-card link :to="project.url">
                    <v-img
                      :src="project.src"
                      class="white--text align-end"
                      gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                      height="200px"
                    >
                      <v-card-title v-text="project.title"></v-card-title>
                      <v-card-subtitle>
                        {{ project.description }}
                      </v-card-subtitle>
                    </v-img>
                    <v-card-actions>
                      <v-chip-group column>
                        <v-chip
                          v-for="skill of project.skills"
                          :key="skill"
                          outlined
                        >
                          {{ skill }}
                        </v-chip>
                      </v-chip-group>
                    </v-card-actions>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import AvatarMenu from "../components/AvatarMenu";
export default {
  components: {
    AvatarMenu,
  },
  computed: {
    filteredProjects() {
      if (!this.selectedStack.length) return this.projects;
      let stack = this.selectedStack.map(i => this.skills[i]);
      return this.projects.filter(project => {
        for (let skill of project.skills) {
          if (stack.includes(skill)) return true;
        }
        return false;
      });
    },
  },
  data() {
    return {
      showMenu: false,
      selectedStack: [],
      skills: [
        "NodeJS",
        "Javascript",
        "Lambda",
        "API Gateway",
        "Linux",
        "CI/CD",
        "Terraform",
        "VueJS",
        "Wordpress",
        "Solidity / Web3",
      ],
      projects: [
        {
          title: "Brazy Proxies Admin Dashboard",
          src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
          flex: 6,
          skills: [
            "NodeJS",
            "Lambda",
            "API Gateway",
            "CI/CD",
            "VueJS",
            "Linux",
          ],
          description:
            "Dashboard that connects back end Squid servers for Admin",
          url: "/portfolio/BrazyProxies",
        },

        {
          title: "Brazy Proxies Residential Dashboard",
          src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
          flex: 6,
          skills: ["Javascript", "Lambda", "API Gateway", "Wordpress"],
          description:
            "Dashboard for users to manage their residential proxy subscription",
          url: "/portfolio/BrazyProxies",
        },
        {
          title: "Dali",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 6,
          skills: ["NodeJS", "Lambda", "API Gateway", "CI/CD", "VueJS"],
          description: "Mobile-first web app that helps users plan their week",
        },
        {
          title: "dApple Tree",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 6,
          skills: ["NodeJS", "CI/CD", "VueJS", "Solidity / Web3"],
          description: "Decentralized procurement powered by Airnode",
        },
      ],
    };
  },
};
</script>
