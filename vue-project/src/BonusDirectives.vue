<template>
  <div>
    <h2 v-once>{{ name }}</h2>
    <button @click="name = 'Batman'">Change Name</button>

    <h2 v-pre>{{ name }}</h2>
  </div>
</template>

<script>
export default {
  name: "BonusDirective",
  data() {
    return {
      name: "Vishwas",
    };
  },
  methods: {},
};
</script>

<style>
</style>