<template>
  <div>
    <v-app-bar flat color="transparent">
      <v-toolbar-title>
        Contact
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
        <v-col
          cols="12"
          lg="6"
          md="6"
          class="d-flex flex-column justify-center align-center"
        >
          <v-card>
            <v-card-title>Web Developer</v-card-title>
            <v-card-subtitle
              >I specialize in AWS Cloud Solutions</v-card-subtitle
            >
            <v-card-text
              >Hi, I'm Camron, a Javascript Developer. I have been coding for 37
              years straight and I would make your company mad good</v-card-text
            >
            <v-card-text
              >Hi, I'm Camron, a Javascript Developer. I have been coding for 37
              years straight and I would make your company mad good</v-card-text
            >
            <v-divider></v-divider>
            <v-card-title>
              Skills
            </v-card-title>
            <v-card-text>
              <v-list>
                <v-list-item>
                  <v-list-item-content>
                    <v-list-item-title>
                      Javascript
                    </v-list-item-title>
                    <v-list-item-subtitle>
                      4 Yrs
                    </v-list-item-subtitle>
                    <v-progress-linear rounded value="90"></v-progress-linear>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item>
                  <v-list-item-content>
                    <v-list-item-title>
                      Vue
                    </v-list-item-title>
                    <v-list-item-subtitle>
                      2 Yrs
                    </v-list-item-subtitle>
                    <v-progress-linear rounded value="50"></v-progress-linear>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn>
                Contact Me
              </v-btn>
              <v-btn>
                Portfolio
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
    return { showMenu: false };
  },
};
</script>
