<template>
  <div>
    <v-app-bar flat color="transparent">
      <v-toolbar-title>
        About Me
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <AvatarMenu />
    </v-app-bar>
    <br />
    <br />
    <v-container fluid pa-0>
      <v-row align="center" justify="center" dense>
        <v-col
          cols="12"
          lg="6"
          md="6"
          class="d-flex flex-column justify-center align-center"
        >
          <v-card>
            <v-card-title>
              <h2>
                Back-End Developer
              </h2>
            </v-card-title>
            <v-card-subtitle>
              I specialize in AWS Cloud Solutions
            </v-card-subtitle>
            <v-card-text>
              Hi, I'm Camron, a Javascript Developer. I got started in
              development in 2016 when I started my proxy business. I quickly
              found my niche with serverless technology. I've picked up a lot of
              helpful skills along the my development journey. It's nice to meet
              you!
            </v-card-text>

            <v-divider></v-divider>
            <v-card-title>
              Skills
            </v-card-title>
            <v-card-text>
              <v-list>
                <v-list-item v-for="skill of skills" :key="skill.title">
                  <v-list-item-content>
                    <v-list-item-title>
                      {{ skill.title }}
                    </v-list-item-title>
                    <v-list-item-subtitle>
                      {{ skill.duration }}
                    </v-list-item-subtitle>
                    <v-progress-linear
                      rounded
                      :value="skill.value"
                    ></v-progress-linear>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn text color="grey" link to="/portfolio">
                Portfolio
              </v-btn>
              <v-btn text color="grey">
                Contact Me
              </v-btn>
            </v-card-actions>
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
  data() {
    return {
      showMenu: false,
      skills: [
        { title: "NodeJS", duration: "4 Years", value: 90 },
        { title: "AWS", duration: "4 Years", value: 70 },
        { title: "Linux", duration: "4 Years", value: 70 },
        { title: "Wordpress", duration: "4 Years", value: 70 },
        { title: "Vue JS", duration: "1 Year", value: 40 },
        { title: "Solidity / Web3", duration: "6 Months", value: 25 },
      ],
    };
  },
};
</script>
