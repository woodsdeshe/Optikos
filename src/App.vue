<template>
  <header>
    <img class="logo" src="../src/assets/png/optikos-high-resolution-logo-color-on-transparent-background.png">
    <HomePage></HomePage>
  </header>
  <nav>
    <router-link class="login" v-bind:to="{ name: 'logout' }" v-if="$store.state.token">Logout</router-link>
    <router-link class="login" v-bind:to="{ name: 'login' }" v-else>Login</router-link>
    <router-link class="product-link" v-bind:to="{ name: 'products'} "> Home</router-link> 
  </nav>
</template>

<script>
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    HomePage
  }
}
</script>

<style>
  .logo {
height:fit-content;
}


</style>
