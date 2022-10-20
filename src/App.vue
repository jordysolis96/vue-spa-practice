<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TopNav from './components/TopNav.vue'
</script>

<template>

  <TopNav />

<!--      <nav>-->
<!--        <RouterLink to="/">Home</RouterLink>-->
<!--        <RouterLink to="/about">About</RouterLink>-->
<!--        <RouterLink to="/exercise">Exercise</RouterLink>-->
<!--        <RouterLink to="/demo">demo</RouterLink>-->
<!--        <RouterLink to="/rps">RPS</RouterLink>-->
<!--        <RouterLink to="/products">products</RouterLink>-->
<!--        <RouterLink to="/checkout">Checkout</RouterLink>-->
<!--        <RouterLink to="/inventory">Inventory</RouterLink>-->


<!--      </nav>-->


  <RouterView />
</template>

<style scoped>

</style>
