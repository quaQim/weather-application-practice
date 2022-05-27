<template>
  <HeaderDispaly />
  <WeatherContent />
</template>

<script>
import HeaderDispaly from "./components/HeaderDisplay.vue";
import WeatherContent from "./components/weather/WeatherContent.vue";
export default {
  name: "App",
  components: {
    HeaderDispaly,
    WeatherContent,
  },
};
</script>

<style></style>
