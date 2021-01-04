<template>
  <div class="products-new">
    <h1>Create New Products</h1>
    <form v-on:submit.prevent="createProduct()">
      <ul>
        <li v-for="error in errors" v-bind:key="error.id">{{ error }}</li>
      </ul>
      <div>
        Name:
        <input type="text" v-model="newProductName" />
      </div>
      <div>
        inventory:
        <input type="text" v-model="newProductIventory" />
      </div>
      <div>
        price:
        <input type="text" v-model="newProductPrice" />
      </div>
      <div>
        image_url:
        <input type="text" v-model="newProductImage_url" />
      </div>
      <input type="submit" value="Create" />
    </form>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data: function() {
    return {
      newProductName: "",
      newProductIventory: "",
      newProductPrice: "",
      newProductImage_url: "",
      errors: [],
    };
  },
  created: function() {},
  methods: {
    createProduct: function() {
      var params = {
        name: this.newProductName,
        inventory: this.newProductIventory,
        price: this.newProductPrice,
        image_url: this.newProductImage_url,
      };
      axios
        .post("/api/products", params)
        .then(response => {
          console.log("Product created", response);
          this.$router.push("/");
        })
        .catch(error => {
          console.log("products create error", error.response);
          this.errors = error.response.data.errors;
        });
    },
  },
};
</script>
