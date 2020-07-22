<template>
  <section class="menu">
    <div v-for="(route,index) in items" :key="index">
      <router-link :to="route.link">{{route.title}}</router-link>
    </div>
  </section>
</template>
<script>
export default {
  name: "Menu",
  data() {
    return {
      drawer: null,
      items: [
        { title: "Lista productos", link: "/", icon: "playlist-edit"},
        { title: "Añadir", link: "/Add", icon: "shape-rectangle-add"},

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