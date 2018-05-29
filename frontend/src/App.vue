<template>
  
  <div id="app">
    <!-- Page navbar, even it's really a hero -->
    <section class="hero is-primary is-bold">
      <div class="hero-body">
        <div class="container">
          <p class="level-item has-text-centered">
            <img src="./assets/logo.png" alt="" style="height: 50px;">
          </p>
          <h1 class="subtitle has-text-centered">
            My source for all vidya songs
          </h1>
        </div>
      </div>
    </section>
    <!-- Component matched by the route will render here -->
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
@import "../node_modules/bulma/css/bulma.min.css";
</style>
