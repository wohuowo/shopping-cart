<template>
  <div id="nav">
    <router-link to="/">Home</router-link>
    <router-link to="/cart">Cart</router-link>
  </div>
  <router-view />
</template>

<script>
export default {
  mounted() {
    this.$store.commit("updateCartFromLocalStorage");
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

html,
body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
body {
  background-color: rgb(245, 245, 245);
}
#nav {
  padding: 10px;
  width: 100%;
  height: 30px;
  background-color: whitesmoke;
  line-height: 30px;
}

#nav a {
  font-weight: bold;
  color: darkslategrey;
  text-decoration: none;
  margin: 0 5px 0 5px;
  font-size: 1.25rem;
}
#nav a.router-link-exact-active {
  color: blueviolet;
}
.text-center {
  text-align: center;
}
</style>
