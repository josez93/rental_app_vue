<!--make sure to comeback and check if this is still working once you add the images to each product -->

<template>
  <div class="Products-show">
    <div>
      <h2>{{ product.name }}</h2>
      <img v-bind:src="`${product.image_url}`" :alt="product.id" />

      <router-link to="/">Back to all products</router-link>
    </div>
    <div>
      <form v-on:summit="createOrder()">
        <ul>
          <li v-for="error in errors" v-bind:key="error.id">{{ error }}</li>
        </ul>
        Quantity:
        <input type="text" v-model="newquantity" />
      </form>
      <button v-on:click="addCart()">Add to Cart</button>
    </div>
    <!-- is Admin Section -->
    <div>
      <button v-on:click="destroyProduct(product)">Destroy product</button>
      <ul v-if="isAdmin()">
        <router-link :to="`/products/${product.id}/edit`">edit</router-link>
      </ul>
    </div>
  </div>
  <!-- end of is admin section -->
</template>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      product: {},
      newquantity: "",
      product_id: "",
      order: {},
      errors: [],
      error: [],
    };
  },
  created: function() {
    axios.get("/api/products/" + this.$route.params.id).then(response => {
      console.log(response.data);
      this.product = response.data;
    });
  },
  methods: {
    destroyProduct: function(product) {
      axios.delete("/api/products/" + product.id).then(response => {
        console.log("product destroyed", response.data);
        this.$router.push("/");
      });
    },
    // isAdmin still doesnt work
    isAdmin: function() {
      if (localStorage.getItem("user_admin")) {
        return true;
      } else {
        return false;
      }
    },
    createOrder: function() {
      var params = {
        quantity: this.newquantity,
        product_id: this.product.id,
      };
      axios
        .post("/api/orders", params)
        .then(response => {
          console.log("order created", response.data);
          this.$router.push("/");
        })
        .catch(error => {
          console.log("order error", error.response);
          this.error = error.response.data.errors;
        });
    },
    addCart: function() {
      var params = {
        quantity: this.newquantity,
        product_id: this.product.id,
      };
      axios
        .post("/api/carted_products", params)
        .then(response => {
          console.log("added to cart", response.data);
          this.$router.push("/carted_products");
        })
        .catch(error => {
          console.log("order error", error.response);
          this.error = error.response.data.errors;
        });
    },
  },
};
</script>
