<template>
  <nav>
    <router-link to="/">Product</router-link> |
    <router-link to="/point">Redeemproduct</router-link>
  </nav>
  <router-view />
</template>

<script>
export default {
  data() {
    return {
      isAdmin: false,
    };
  },
  mounted() {
    console.log("aaaaaa");
    // if (localStorage.get("isAdmin")) this.isAdmin = true;
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

nav a {
  font-weight: bold;
  color: #ffffff;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
