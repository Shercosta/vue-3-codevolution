<template>
  <div>
    <h2>Volume Tracker (0 - 20)</h2>
    <h3>Current Volume - {{ volume }}</h3>
    <div>
      <button @click="volume += 2">Increase</button>
      <button @click="volume -= 2">Decrease</button>
    </div>

    <input type="text" name="" v-model="movie" id="" />
    <input type="text" name="" v-model="movieInfo.title" id="" />
    <input type="text" name="" v-model="movieInfo.actor" id="" />

    <div>
      <button @click="movieList = movieList.concat(['Wonder Woman'])">
        Add Movie
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Watchers",
  data() {
    return {
      volume: 0,
      movie: "Batman",
      movieInfo: {
        title: "",
        actor: "",
      },
      movieList: ["Batman", "Sumerpan"],
    };
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert("Warning more than 16");
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Calling API with movie name = ${newValue}`);
      },
      immediate: true,
    },
    movieInfo: {
      handler(newValue) {
        console.log(`TItle = ${newValue.title} actor = ${newValue.actor}`);
      },
      deep: true,
    },
    movieList: {
      handler(newValue) {
        console.log(newValue);
      },
      // deep: true,
    },
  },
};
</script>

<style></style>
