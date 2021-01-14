<template>
  <div class="carted-products">
    <h1>This Is Your Cart</h1>
    <div v-for="carted_product in carted_products" v-bind:key="carted_product.id">
      <img v-bind:src="`${carted_product.product.image_url}`" alt="carted_product.id" />
      <p>Quantity: {{ carted_product.quantity }}</p>
      <button v-on:click="removeFromCart(carted_product)">remove product from cart</button>
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
      carted_product: {},
    };
  },
  created: function() {
    axios.get("/api/carted_products").then(response => {
      this.carted_products = response.data;
      console.log(this.carted_products);
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
    removeFromCart: function(carted_product) {
      axios.delete("/api/carted_products/" + carted_product.id).then(response => {
        console.log("removed from cart", response.data);
        this.carted_products.splice(this.carted_products.indexOf(carted_product), 1);
      });
    },
  },
};
</script>
