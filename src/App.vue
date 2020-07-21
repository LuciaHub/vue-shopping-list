<template>
  <div>
    <v-app-bar>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>Mi lista de la compra</v-toolbar-title>
      
      <v-menu>
        <template>
          <v-btn>
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item>
            v-for="n in 5"
            :key="n"
            @click="() => {}"
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>

      </v-menu>
    </v-app-bar>
  </div>
</template>