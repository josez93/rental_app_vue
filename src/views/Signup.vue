<template>
  <div class="signup">
    <div class="col-lg-5 col-md-10">
      <div class="contact-form">
        <form class="contact-form-style" v-on:submit.prevent="submit()">
          <h1>
            <strong></strong>
            Signup
          </h1>
          <ul>
            <li class="text-danger" v-for="error in errors" v-bind:key="error.id">{{ error }}</li>
          </ul>
          <div class="form-group">
            <label><strong>First Name:</strong></label>
            <input type="text" class="form-control" v-model="first_name" />
          </div>
          <div class="form-group">
            <label><strong>Last Name:</strong></label>
            <input type="text" class="form-control" v-model="last_name" />
          </div>
          <div class="form-group">
            <label><strong>Street Address:</strong></label>
            <input type="text" class="form-control" v-model="street_address" />
          </div>
          <div class="form-group">
            <label>
              <strong>Phone Number</strong>
              :
            </label>
            <input type="text" class="form-control" v-model="phone_number" />
          </div>
          <div class="form-group">
            <label><strong>Email:</strong></label>
            <input type="email" class="form-control" v-model="email" />
          </div>
          <div class="form-group">
            <label><strong>Password:</strong></label>
            <input type="password" class="form-control" v-model="password" />
          </div>
          <div class="form-group">
            <label><strong>Password confirmation:</strong></label>
            <input type="password" class="form-control" v-model="passwordConfirmation" />
            <small v-if="password !== passwordConfirmation" class="text-danger">
              Must match password
            </small>
          </div>
          <input type="submit" class="btn btn-primary" value="Submit" />
        </form>
      </div>
      <p class="form-messege"></p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      first_name: "",
      last_name: "",
      street_address: "",
      email: "",
      phone_number: "",
      password: "",
      passwordConfirmation: "",
      errors: [],
    };
  },
  methods: {
    submit: function() {
      var params = {
        first_name: this.first_name,
        last_name: this.last_name,
        street_address: this.street_address,
        email: this.email,
        phone_number: this.phone_number,
        password: this.password,
        password_confirmation: this.passwordConfirmation,
      };
      axios
        .post("/api/users", params)
        // eslint-disable-next-line no-unused-vars
        .then(response => {
          this.$router.push("/login");
        })
        .catch(error => {
          this.errors = error.response.data.errors;
        });
    },
  },
};
</script>
