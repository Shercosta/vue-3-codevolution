<script>
import Greet from "./components/Greet.vue";
import Article from "./components/Article.vue";

export default {
  name: "App",
  components: {
    Greet,
    Article,
  },
  data() {
    return {
      name: "Shercos",
      channel: "SCT Content",
    };
  },
};
</script>

<template>
  <div class="wrapper"></div>
  <!-- <Greet name="Bruce" hero-name="Batman" />
  <Greet name="Clark" hero-name="Superman" />
  <Greet name="Diana" hero-name="Wonder Woman" />
  <Greet :name="name" :hero-name="channel" /> -->

  <Article title="Article Title" :likes="50" :isPublished="true" />
  <main></main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
