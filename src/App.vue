<template>
  <div id="app">
    <div id="nav" class="flex justify-between max-w-xl mx-auto text-xl">
      <router-link to="/">Home</router-link>
      <router-link to="/jokes">All Jokes</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
import { mapActions } from "vuex"
export default {
  methods: {
    ...mapActions(["setCurrentJoke"]),
  },
  mounted() {
    this.setCurrentJoke()
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #707374;
}

#nav {
  padding: 1.2rem 4.2rem;
}

#nav a {
  font-weight: bold;
  color: #707374;
  text-decoration: none;
  letter-spacing: 0.1rem;
}

#nav a.router-link-exact-active {
  color: #2196f3;
}
</style>
