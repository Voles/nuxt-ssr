<template>
  <div>
    <h1 class="title">{{title}}</h1>
    <h2 class="degrees" v-if="degrees">{{degrees}}°C</h2>
  </div>
</template>

<script>
  export default {
    name: 'Weather',
    props: ['title', 'degrees']
  }
</script>

<style scoped>
  .title {
    font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }

  .degrees {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
  }
</style>
