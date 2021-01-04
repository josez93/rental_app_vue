<template>
  <div class="Products-edit">
    <h1>Edit Products</h1>

    <form v-on:summit.prevent="updateProducts(product)">
      <ul>
        <li v-for="error in errors" v-bind:key="error.id">{{ error }}</li>
      </ul>
      <div class="form-group">
        <label>name:</label>
        name:
        <input type="text" v-model="product.name" />
      </div>
      <div class="form-group">
        inventory:
        <input type="text" v-model="product.inventory" />
      </div>
      <div class="form-group">
        price:
        <input type="text" v-model="product.price" />
      </div>
      <div class="form-group">
        image_url:
        <input type="text" v-model="product.image_url" />
      </div>
      <input type="submit" class="btn btn-primary" value="Submit" />
    </form>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      errors: [],
      product: {},
    };
  },
  created: function() {
    axios.get("/api/products/" + this.$route.params.id).then(response => {
      this.product = response.data;
    });
  },
  methods: {
    updateProducts: function(product) {
      var params = {
        name: product.name,
        inventory: product.inventory,
        price: product.price,
        image_url: product.image_url,
      };
      axios
        .patch("/api/products/" + product.id, params)
        .then(response => {
          console.log("products updated", response);
          this.$router.push("/");
        })
        .catch(error => {
          this.errors = error.response.data.errors;
        });
    },
  },
};
</script>
