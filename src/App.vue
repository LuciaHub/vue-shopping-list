<template>
  <v-app>
    <v-navigation-drawer app><Menu/></v-navigation-drawer>
    <v-app-bar app> 
      <v-row align="center" justify="center">
        Lista de la compra
      </v-row>
    </v-app-bar>
  </v-app>
</template>
<script>
import Menu from './menu/menu';
export default {
  name: "App",
   data(){
    return {
      drawer: false
    }
  },
  components: {
    Menu
  }
};
</script>