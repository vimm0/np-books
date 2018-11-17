<template>
  <div class="container">
    <h1 class="is-size-2 has-text-centered" v-if="error.statusCode === 404">Page not found</h1>
    <h1 class="is-size-2 has-text-centered" v-else>An error occurred</h1>
    <div class="button has-text-centered">
      <nuxt-link class="button" to="/">Return Home page</nuxt-link>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['error'],
  }
</script>
<style>
  div.button{
    margin-top:2rem;
  }
</style>
