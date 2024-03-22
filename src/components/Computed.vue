<template>
  <div>
    <h3>Computed fullname - {{ fullName }}</h3>
  </div>

  <button @click="items.push({ id: 4, title: 'Infinix Hot', price: 10000 })">
    Add Item
  </button>

  <div>
    <h3>Computed Total - {{ total }}</h3>
  </div>

  <hr />
  <template v-for="item in items" :key="item.id">
    <h3 v-if="item.price > 6000">{{ item.title }} {{ item.price }}</h3>
    <h3 v-for="item in expensiveItems" :key="item.id">
      Computed Expensive {{ item.title }} {{ item.price }}
    </h3>
  </template>
</template>

<script>
export default {
  data() {
    return {
      firstName: "Mickyas",
      lastName: "Zenebe",
      items: [
        {
          id: 1,
          title: "Samsung A10",
          price: 5500,
        },
        {
          id: 2,
          title: "Samsung A30",
          price: 9500,
        },
        {
          id: 3,
          title: "Samsung A70",
          price: 20000,
        },
      ],
    };
  },

  methods: {},

  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
    expensiveItems() {
      return this.items.filter((item) => item.price > 7000);
    },
  },
};
</script>
