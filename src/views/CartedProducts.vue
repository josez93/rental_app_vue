<template>
  <div class="carted-products">
    <h1>this is cart</h1>
    <div v-for="carted_product in carted_products" v-bind:key="carted_product.id">
      <img v-bind:src="`${carted_product.product.image_url}`" alt="carted_product.id" />
      <p>Quantity: {{ carted_product.quantity }}</p>
    </div>
    <button v-on:click="createOrder">create order</button>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      carted_products: [],
    };
  },
  created: function() {
    axios.get("/api/carted_products").then(response => {
      console.log("cart index", response);
      this.carted_products = response.data;
    });
  },
  methods: {
    createOrder: function() {
      var params = {
        quantity: this.quantity,
      };
      axios
        .post("/api/orders", params)
        .then(response => {
          console.log("order created", response);
          this.$router.push("/");
        })
        .catch(error => {
          console.log("photos create error", error.response);
          this.errors = error.response.data.errors;
        });
    },
  },
};
</script>
