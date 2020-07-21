<template>
  <section class="menu">
    <div v-for="(route,index) in routes" :key="index">
      <MenuItem :data="route"/>
    </div>
  </section>
</template>
<script>
  export default {
      name: "Menu",
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Lista productos' }
        ],
      }
    },
  }
</script>


<style scoped>
.menu {
  background-color: #040505;
  width: 300px;
  height: 100%;
}
</style>