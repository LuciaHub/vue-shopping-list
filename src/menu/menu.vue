<template>
  <v-sheet height="400" class="overflow-hidden" style="position: relative;">
         <v-toolbar dense color="purple" dark flat>
        <v-list-item>

          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title >Mi lista de la compra</v-list-item-title>
         
        </v-list-item>
         </v-toolbar>


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
        { title: "Lista productos", icon: "playlist-tick", link: "/" },
        { title: "Añadir", icon: "cart-plus", link: "/add" },
        
      ],
    };
  },
};
</script>