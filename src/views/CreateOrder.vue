<template>
  <div class="order-new">
    <div>
      <form v-on:summit.prevent="createOrder()">
        <ul>
          <li v-for="error in errors" v-bind:key="error.id">{{ error }}</li>
        </ul>
        Quantity:
        <input type="text" v-model="newquantity" />
      </form>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      newquantity: "",
      newproduct_id: "",
      errors: [],
    };
  },
  created: function() {},
  methods: {
    createOrder: function() {
      var params = {
        quantity: this.newquantity,
        product: this.newproduct_id,
      };
      axios
        .post("/api/orders", params)
        .then(response => {
          console.log("order created", response);
          this.$router.push("/");
        })
        .catch(error => {
          console.log("order error", error.response);
          this.error = error.response.data.errors;
        });
    },
  },
};
</script>
