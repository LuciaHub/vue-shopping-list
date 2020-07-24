<template>
<div class="Add">
    <v-form>
      <v-container>
        <v-row>
  
          <v-col cols="12" sm="6" md="3">
             <v-text-field
               label="Producto"
             ></v-text-field>
          </v-col>
          <v-col cols="12" sm="6" md="3">
             <v-text-field
               label="Cantidad"
             ></v-text-field>
          </v-col>
        </v-row>
      </v-container>
    </v-form>
</div>
</template>
  
<script>

export default {
  name: "Add",

  data: () => ({
    valid: true,
    Producto: "",
    cantidad: "",
  }),

    methods: {
    reset() {
      this.$refs.form.reset();
    },
    crear(){
      console.log(this.model);
    }
  },
 
};
</script>


