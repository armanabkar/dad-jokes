<template>
  <div>
    <h1 class="text-2xl pb-4 px-12 font-extrabold border-b-2">
      This is all the jokes you've retrieved:
    </h1>
    <h4 v-for="(joke, idx) in jokes" :key="idx">
      <span>{{ idx + 1 }}~</span>
      {{ joke }}
    </h4>
  </div>
</template>
<script>
import { mapGetters } from "vuex"
export default {
  computed: {
    ...mapGetters({
      jokes: "getAllJokes",
    }),
  },
}
</script>
<style scoped>
h4 {
  color: #2196f3;
  font-weight: bolder;
  font-size: 1.5rem;
  padding: 0 1.5rem;
  margin: 0.5rem;
}

h4 span {
  color: #707374;
}
</style>
