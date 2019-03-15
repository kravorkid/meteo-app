<template>
  <div class="col-8 mx-auto">
    <div class="form-group">
      <label for="getWeather">Enter a city to search for weather</label>
      <input type="text" name="getWeather" v-model="city" class="form-control">
    </div>
    <button type="button" v-on:click="getWeather" name="button">Search For Weather</button>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'SearchInput',
  data () {
    return {
      city: ''
    }
  },
  methods: {
    async getWeather () {
      try {
        const res = await axios.get(`https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=63310492d642eb1d0c68a2d318b6e786`)
        this.weatherInfo = res.data
      } catch (err) {
        this.weatherInfo = false
        console.log(err)
      }
      return this.weatherInfo
    }
  }
}
</script>

<style lang="css" scoped>
</style>
