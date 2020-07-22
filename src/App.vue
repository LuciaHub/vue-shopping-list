<template>
  <v-app>
    <v-navigation-drawer app><Menu/></v-navigation-drawer>
    <v-app-bar app>Mi lista de la compra</v-app-bar>
    <v-main>Main</v-main>
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