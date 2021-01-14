<template>
  <div class="login">
    <div class="col-lg-12 col-md-20">
      <div class="contact-form">
        <form v-on:submit.prevent="submit()">
          <h1>Login</h1>
          <ul>
            <li class="text-danger" v-for="error in errors" v-bind:key="error.id">{{ error }}</li>
          </ul>
          <div class="form-group">
            <label>Email:</label>
            <input type="email" class="form-control" v-model="email" />
          </div>
          <div class="form-group">
            <label>Password:</label>
            <input type="password" class="form-control" v-model="password" />
          </div>
          <input type="submit" class="btn btn-primary" value="Submit" />
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      email: "",
      password: "",
      errors: [],
    };
  },
  methods: {
    submit: function() {
      var params = {
        email: this.email,
        password: this.password,
      };
      axios
        .post("/api/sessions", params)
        .then(response => {
          axios.defaults.headers.common["Authorization"] = "Bearer " + response.data.jwt;
          localStorage.setItem("jwt", response.data.jwt);
          localStorage.setItem("user_id", response.data.user_id);
          localStorage.setItem("user_admin", response.data.user_admin);
          this.$router.push("/");
          console.log(response.data);
        })
        // eslint-disable-next-line no-unused-vars
        .catch(error => {
          this.errors = ["Invalid email or password."];
          this.email = "";
          this.password = "";
        });
    },
  },
};
</script>
