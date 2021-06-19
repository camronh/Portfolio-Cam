<template>
  <div>
    <v-app-bar flat>
      <v-toolbar-title>
        About Me
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-avatar>
        <img
          src="https://randomuser.me/api/portraits/women/81.jpg"
          alt="logo"
        />
      </v-avatar>
      <p class="ml-3">
        Camron Haider
      </p>
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
            <v-card-subtitle>I specialize in AWS Cloud Solutions</v-card-subtitle>
            <v-card-text>Hi, I'm Camron, a Javascript Developer. I have been coding for 37 years straight and I would make your company mad good</v-card-text>
            <v-card-text>Hi, I'm Camron, a Javascript Developer. I have been coding for 37 years straight and I would make your company mad good</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import ProfileCard from "../components/Header";

export default {
  components: {
    ProfileCard,
  },
};
</script>
