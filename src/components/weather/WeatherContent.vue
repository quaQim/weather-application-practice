<template>
  <div class="weather-wrapper">
    <ContentHeader />
    <CitySelector @selectCity="selectCity" />
    <WeatherList :weatherList="weatherList" />
    <link
      href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,800&display=swap"
      rel="stylesheet"
    />
  </div>
</template>

<script>
import weatherMixin from "@/mixins/weatherMixin";
import ContentHeader from "./ContentHeader.vue";
import CitySelector from "./CitySelector";
import WeatherList from "./WeatherList";
export default {
  name: "weather-content",
  components: {
    ContentHeader,
    CitySelector,
    WeatherList,
  },
  mixins: [weatherMixin],
  data() {
    return {
      weatherList: [],
    };
  },
  methods: {
    async selectCity(city) {
      if (city.selected) {
        const weather = await this.getWeatherInfo(city);
        this.weatherList.push(weather);
      } else {
        const index = this.weatherList.findIndex(
          (weather) => weather.code === city.code
        );
        this.weatherList.splice(index, 1);
      }
    },
  },
};
</script>

<style scoped>
.weather-wrapper {
  font-family: "Playfair Display", serif;
}
</style>
