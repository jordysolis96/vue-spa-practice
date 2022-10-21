<script setup>
// Using const because props are READ-ONLY and should not be changed.
const props = defineProps(['userData', 'greeting'])

// const props = defineProps({
//        greeting: String,
//        otherProp: Number,
//        userData: {
//          type: Object,
//          default: {
//
//          }
//        }
//    })
console.log(props.greeting);
console.log(props.userData)

</script>

<template>
  <div class="topnav">
    <RouterLink class="link-item" to="/">Home</RouterLink>
    <RouterLink class="link-item" to="/about">About</RouterLink>
    <RouterLink class="link-item" to="/exercise">Exercise</RouterLink>
    <RouterLink class="link-item" to="/demo">demo</RouterLink>
    <RouterLink class="link-item" to="/rps">RPS</RouterLink>
    <RouterLink class="link-item" to="/products">products</RouterLink>
    <RouterLink class="link-item" to="/checkout">Checkout</RouterLink>
    <RouterLink class="link-item" to="/inventory">Inventory</RouterLink>
    <p class="link-item" style="color: #04AA6D">Welcome, {{ userData.username }}!</p>
<!--    to access userData when props takes in an object-->
<!--    <p class="link-item" style="color: #04AA6D">Welcome, {{ props.userData.username }}!</p>-->
  </div>

</template>

<style scoped>
/* Add a black background color to the top navigation */
.topnav {
  background-color: #333;
  overflow: hidden;
}

/* Style the links inside the navigation bar */
.topnav .link-item {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

/* Change the color of links on hover */
.topnav .link-item:hover {
  background-color: #ddd;
  color: black;
}

/* Add a color to the active/current link */
.topnav .link-item:active {
  background-color: #04AA6D;
  color: white;
}

</style>
