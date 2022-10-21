<!--The content here will appear on every page-->
<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TopNav from './components/TopNav.vue'
let user = {
  id: 922022,
  username: "CodeyThaDuck",
  password: "gocodeup",
  themePreference: "dark-theme",
  email: "codey@codeup.com"
}

let preference = user.themePreference;
</script>

<template>
<!--  <html v-bind:class="preference">-->
  <TopNav v-bind:user-data="user" />

  <RouterView />

<!--  <main class="container d-flex justify-content-center">-->
<!--    &lt;!&ndash;references the value of our 'preference' variable&ndash;&gt;-->
<!--    <form v-bind:class="preference" class="w-50 p-3">-->
<!--      <h2>Login</h2>-->
<!--      <label for="username" class="form-label">Username</label>-->
<!--      <input type="text" id="username" name="username" class="form-control">-->
<!--      <label for="password" class="form-label">Password</label>-->
<!--      <input type="password" id="password" name="password" class="form-control">-->
<!--      <div class="text-center mt-3">-->
<!--        &lt;!&ndash;references the value of our 'preference' variable (shorthand)&ndash;&gt;-->
<!--        <button :class="preference" class="w-50" type="submit">Login</button>-->
<!--      </div>-->
<!--    </form>-->
<!--  </main>-->
<!--  </html>-->
</template>

<style scoped>
.dark-theme {
  background-color: #020403; /* Obsidian black */
  color: whitesmoke;
}

.hufflepuff-theme {
  background-color: goldenrod;
  color: #020403; /* Obsidian black */
}
</style>
