<template>
  <div>
    <ul class="weather-list">
      <WeatherItem
        v-for="weather in weatherList"
        :key="weather.code"
        :weather="weather"
      />
    </ul>
  </div>
</template>

<script>
import WeatherItem from "./WeatherItem.vue";
export default {
  name: "Weather-List",
  components: { WeatherItem },
  props: { weatherList: Array },
};
</script>

<style scoped>
.weather-list {
  display: grid;
  grid-gap: 1em;
  margin-top: 1em;
  grid-template-columns: repeat(5, 1fr);
}
</style>
