<template>
  <div>
    <h2>Volume Tracker (0 - 20)</h2>
    <h3>Current Volume - {{ volume }}</h3>
    <div>
      <button @click="volume += 2">Increase</button>
      <button @click="volume -= 2">Decrease</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Watchers",
  data() {
    return {
      volume: 0,
    };
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if(newValue > oldValue && newValue === 16) {
        alert("Warning more than 16")
      }
    }
  },
};
</script>

<style>
</style>