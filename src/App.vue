<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      |
      <router-link to="/signup">Signup</router-link>
      |
      <router-link to="/login">Log in</router-link>
      |
      <router-link to="/logout">Log out</router-link>
      |
      <router-link to="/productsNew">New Products</router-link>
      |
    </div>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
export default {
  methods: {
    getUserId: function() {
      return localStorage.getItem("user.id");
    },
  },
  isLoggedIn: function() {
    if (localStorage.getItem("jwt")) {
      return true;
    } else {
      return false;
    }
  },
  // here goes is Admin when its fixed **rememeber to add ${} to interpolate also call with $parent.
};
</script>
