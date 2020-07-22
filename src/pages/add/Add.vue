<template>
  <div class='conter'>
    <template>
      <v-form ref="form" v-model="valid" lazy-validation class='form'>

        <v-text-field :rules="productRules" label="Producto" required></v-text-field>
        <v-text-field label="Cantidad" :rules="cantidadRules" required></v-text-field>
        <v-btn :disabled="!valid" color="success" class="mr-4" @click=created validate >Crear</v-btn>
        <v-btn color="error" class="mr-4" @click="reset">Reset Form</v-btn>

      </v-form>
    </template>
  </div>
</template>
  


<script>
import axios from 'axios';
export default {
  name: "Add",

  data: () => ({
    valid: true,
    Producto: "",
    cantidad: "",
  }),

  methods: {
    validate() {
      this.$refs.form.validate();
    },
    reset() {
      this.$refs.form.reset();
    },
    resetValidation() {
      this.$refs.form.resetValidation();
    },
    editar() {
     this.$refs.form.disabled();
    },
      
    created() {
      let post = {
      Producto: '',
      cantidad: '',
      bought: false
  };
    axios.post("http://localhost:3005/items", post).then((result) => {
      console.log(result);
    } );
 
  }
   
  }
};
</script>


