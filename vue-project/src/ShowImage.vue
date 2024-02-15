<template>
  <div>
    <button @click="toggleShow()">Click me!</button>
    <div v-show="showText">
      <h2>This Text</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "ShowImage",
  data() {
    return {
      showText: true,
    };
  },
  methods: {
    toggleShow() {
      this.showText = !this.showText;
    },
  },
};
</script>

<style>
</style>