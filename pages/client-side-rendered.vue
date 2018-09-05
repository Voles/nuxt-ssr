<template>
  <div>
    <weather-loader></weather-loader>
    <nuxt-link to="/" class="button--grey">❮</nuxt-link>
  </div>
</template>

<script>
  import WeatherLoader from '../components/WeatherLoader';

  export default {
    name: "client-side-rendered",
    components: {
      WeatherLoader
    }
  }
</script>

<style scoped>

</style>
