<template>
  <div>
    <weather :title="city" :degrees="degrees"></weather>
    <nuxt-link to="/" class="button--grey">❮</nuxt-link>
  </div>
</template>

<script>
  import fetch from 'node-fetch';
  import Weather from '../../components/Weather';

  export default {
    name: "server-side-rendered",
    components: {
      Weather
    },
    asyncData ({ params }) {
      return fetch(`http://api.openweathermap.org/data/2.5/weather?q=${params.city}&units=metric&apikey=1118b6db1f7e9fa55947c938d0fa8e1f`)
        .then(response => response.json())
        .then(json => ({ city: params.city, degrees: json.main.temp }))
    }
  }
</script>
