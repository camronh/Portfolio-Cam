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
                v-model="selection"
                active-class="primary--text"
                multiple
              >
                <v-chip>Extra Soft</v-chip>
                <v-chip>Soft</v-chip>
                <v-chip>Medium</v-chip>
                <v-chip>Hard</v-chip>
              </v-chip-group>
            </v-card-text>
            <v-divider></v-divider>
            <v-container fluid>
              <v-row dense>
                <v-col
                  v-for="card in cards"
                  :key="card.title"
                  :cols="card.flex"
                >
                  <v-card>
                    <v-img
                      :src="card.src"
                      class="white--text align-end"
                      gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                      height="200px"
                    >
                      <v-card-title v-text="card.title"></v-card-title>
                    </v-img>

                    <v-card-actions>
                      <v-spacer></v-spacer>

                      <v-btn icon>
                        <v-icon>mdi-heart</v-icon>
                      </v-btn>

                      <v-btn icon>
                        <v-icon>mdi-bookmark</v-icon>
                      </v-btn>

                      <v-btn icon>
                        <v-icon>mdi-share-variant</v-icon>
                      </v-btn>
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
  data() {
    return {
      showMenu: false,
      cards: [
        {
          title: "Pre-fab homes",
          src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
          flex: 6,
        },
        {
          title: "Favorite road trips",
          src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
          flex: 6,
        },
        {
          title: "Best airlines",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 6,
        },
      ],
    };
  },
};
</script>
