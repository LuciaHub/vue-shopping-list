<template>
  <v-app>
    <v-navigation-drawer app><Menu/></v-navigation-drawer>
    <v-app-bar app>Lista de la compra</v-app-bar>
  </v-app>
</template>
<script>
import Menu from './menu/menu';
export default {
  name: "App",
  components: {
    Menu
  }
};
</script>

