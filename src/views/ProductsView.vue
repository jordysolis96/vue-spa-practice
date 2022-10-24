<script setup>
import {products} from "../data/products.js";
import ProductCard from "../components/ProductCard.vue";

let product = {
  title: "berserk vol.1",
  description: "This ultraviolent fantasy manga is the first in a series about a cursed lone wanderer with a tragic fate and a cast of bio-horror demons.",
  price: "$49.99",
  image: "https://m.media-amazon.com/images/I/513rmAmf1CL._SX218_BO1,204,203,200_QL40_FMwebp_.jpg"
}

console.log(products);
</script>
<template>
  <h1>This is the product page</h1>
<!--  <ProductCard v-bind:product-data="product"/>-->
  <ProductCard v-bind:product-data="products"/>
</template>