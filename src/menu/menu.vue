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
      items: [{ title: "Lista productos", link: "/" }]
    };
  }
};
</script>


<style scoped>
.menu {
  background-color: rgb(red, green, blue);
  width: 200px;
  height: 100%;
  text-align: center;

  
}
</style>