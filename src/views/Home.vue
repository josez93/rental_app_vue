<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div v-for="product in products" v-bind:key="product.id">
      <img v-bind:src="`${product.image_url}`" alt="" />
      <h1>{{ product.name }}</h1>
      <h2>{{ product.price }}</h2>
      <h3>inventory {{ product.inventory }}</h3>
      <router-link v-bind:to="`/products/${product.id}`">More details</router-link>
    </div>
  </div>
</template>

<style></style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      message: "Rental Business App ",
      products: [],
    };
  },
  created: function() {
    axios.get("/api/products").then(response => {
      console.log("products index", response);
      this.products = response.data;
    });
  },
  methods: {},
};
</script>
