<template>
  <div>
    <weather title="Haarlem" :degrees="degrees"></weather>
  </div>
</template>

<script>
  import fetch from 'node-fetch'
  import Weather from '../components/Weather';

  export default {
    name: "WeatherLoader",
    components: {
      Weather
    },
    data() {
      return {
        degrees: null
      }
    },
    created() {
      this.loadWeatherData()
    },
    methods: {
      loadWeatherData: function () {
        fetch(`http://api.openweathermap.org/data/2.5/weather?q=Haarlem&units=metric&apikey=1118b6db1f7e9fa55947c938d0fa8e1f`)
          .then(response => response.json())
          .then(json => {
            this.degrees = json.main.temp
          })
      }
    }
  }
</script>
