<template>
  <div>
    <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
    <h2>Computed Fullname {{ fullName }}</h2>
    <button @click="items.unshift({ id: 4, title: 'Keyboar', price: 500 })">
      Add Item
    </button>
    <h2>Computed Total = {{ total }}</h2>
    <h2>Method Total = {{ getTotal() }}</h2>
    <input type="text" name="" id="" v-model="country" />

    <template v-for="item in items" :key="item.id">
      <h2 v-if="item.price > 100">{{ item.title }} {{ item.price }}</h2>
    </template>

    <h2 v-for="item in expensiveItems" :key="item.id">
      {{ item.title }} {{ item.price }}
    </h2>
  </div>
</template>

<script>
export default {
  name: "ComputedProperties",
  data() {
    return {
      firstName: "Bruce",
      lastName: "Wayne",
      items: [
        {
          id: 1,
          title: "TV",
          price: 100,
        },
        {
          id: 2,
          title: "Phone",
          price: 200,
        },
        {
          id: 3,
          title: "Laptop",
          price: 300,
        },
      ],
      country: "",
    };
  },
  methods: {
    getTotal() {
      console.log("getTotal Method");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      console.log("total Computed Property");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
    expensiveItems() {
      return this.items.filter((item) => item.price > 100);
    },
  },
};
</script>

<style>
</style>