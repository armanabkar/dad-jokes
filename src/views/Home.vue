<template>
  <div class="home shadow max-w-2xl mx-auto p-8 rounded">
    <h2 class="text-3xl text-blue-500 font-extrabold mb-2">
      Can I Haz Dad Jokes
    </h2>
    <h3 class="h-40 text-black mb-20">{{ joke }}</h3>
    <button
      class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-2 rounded shadow mt-20 focus:outline-none"
      @click="addJoke"
    >
      New Joke!
    </button>
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex"
export default {
  name: "Home",
  methods: {
    ...mapActions({ addJoke: "setCurrentJoke" }),
  },
  computed: {
    ...mapGetters({ joke: "getCurrentJoke" }),
  },
}
</script>

<style scoped>
.home {
  height: 30rem;
  max-height: 35rem;
}
h3 {
  font-size: 1.8rem;
}
</style>
