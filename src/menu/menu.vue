<template>
  <v-sheet height="400" class="overflow-hidden" style="position: relative;">
 
      <v-toolbar dense color="blue" dark flat>

        <v-list-item>
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title >Lista de la compra</v-list-item-title>
        </v-list-item>
      </v-toolbar>
      <v-divider></v-divider>

      <v-list dense>
        <v-list-item v-for="item in items" :key="item.title" link>
          <router-link :to="item.link">
            <v-list-item>
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title text>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
            </v-list-item>
          </router-link>
        </v-list-item>
      </v-list>


  </v-sheet>
</template>
<script>
export default {
  name: "Menu",
  data() {
    return {
      drawer: null,
      items: [
        { title: "Lista productos", link: "/", icon: "playlist-edit"},
        { title: "Añadir", link: "/Add", icon: "cart-plus"},
      ]
      
    };
  }
};
</script>


<style scoped>
.menu {
  background-color: rgb(215, 210, 226);
  width: 100%;
  height: 100vh;
  text-align: center;
}
</style>