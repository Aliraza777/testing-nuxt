<template>
  <div class="container">
    <div class="row">
    <div class="col-6">
      <h1>
      Random facts
    </h1>
    </div>
      <div class="col-6 pt-5">
    <ul class="List">
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/facts">Facts</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul>
      </div>
    </div>
    <hr>
  </div>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>


<style>
body{
  background: white;
}
h1{
  color: black;
}
.List{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
