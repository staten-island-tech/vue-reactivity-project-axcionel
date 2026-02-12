<template lang="">
    <h1>Draft Your Team</h1>
    <li v-for="people in draftees" :key="people.name">
        {{ people.name }} - ${{ people.price }}
    </li>
</template>

<script setup>
import { ref } from 'vue';
const draftees = ref([
  { name: "20 Piece McNuggets", price: 4.99, type: "sides" },
  { name: "McChicken", price: 3.99, type: "sandwiches" },
  { name: "Large Fries", price: 3.99, type: "sides" },
  { name: "McFlurry", price: 4.39, type: "desserts" },
  { name: "Big Mac", price: 6.99, type: "sandwiches" },
  { name: "Snack Wrap", price: 2.99, type: "sides" },
  { name: "Spicy McCrispy", price: 3.99, type: "sandwiches" },
  { name: "Egg McMuffin", price: 3.99, type: "sandwiches" },
  { name: "Sausage Burrito", price: 2.99, type: "sides" },
  { name: "Filet-O-Fish", price: 3.99, type: "sandwiches" },
  { name: "Vanilla Ice Cream", price: 2.99, type: "desserts" },
  { name: "Apple Pie", price: 2.99, type: "desserts" },
  { name: "Happy Meal", price: 6.99, type: "combos" },
  { name: "Quarter Pounder", price: 3.99, type: "sandwiches" },
  { name: "Sausage McMuffin with Egg Meal", price: 6.99, type: "combos" },
  { name: "Big Mac Meal", price: 7.99, type: "combos" },
  { name: "Spicy Deluxe McCrispy Meal", price: 7.99, type: "combos" },
  { name: "Spicy Snack Wrap Meal", price: 5.99, type: "combos" },
  { name: "Sausage Biscuit with Egg", price: 3.99, type: "sandwiches" },
  { name: "Bacon Egg and Cheese McGriddle", price: 3.99, type: "sandwiches" }
]);
</script>


<style lang="">

</style>