<template>
  <v-menu v-model="showMenu" absolute offset-y style="max-width: 600px">
    <template v-slot:activator="{ on, attrs }">
      <p class="ml-3" v-bind="attrs" v-on="on">
        Camron Haider
      </p>
      <v-avatar v-bind="attrs" v-on="on">
        <img
          src="https://randomuser.me/api/portraits/women/81.jpg"
          alt="logo"
        />
      </v-avatar>
    </template>
    <v-list nav flat>
      <v-list-item-group v-model="selectedItem" color="primary" dark required>
        <v-list-item link to="/">
          <v-list-item-title>About</v-list-item-title>
        </v-list-item>
        <v-list-item link to="/portfolio">
          <v-list-item-title>Portfolio</v-list-item-title>
        </v-list-item>
        <v-list-item link to="/contact">
          <v-list-item-title>Contact</v-list-item-title>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  data() {
    return {
      selectedItem: false,
      showMenu: false,
    };
  },
};
</script>
