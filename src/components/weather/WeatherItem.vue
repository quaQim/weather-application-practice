<template>
  <li class="weather-item">
    <h3>{{ weather.label }}</h3>
    <p class="temperature">{{ weather.temperature }}&deg;c</p>
    <p class="info">
      <img :src="weather.icon" alt="any" />
    </p>
    <p class="rest">
      <span>HUM: {{ weather.humidity }}</span>
      <span><br />wind: {{ weather.wind }}m/s</span>
    </p>
  </li>
</template>

<script>
export default {
  name: "weather-Item",
  props: {
    weather: {
      type: Object,
      default() {
        return {
          label: "Seoul",
          code: "seoul",
          temperature: 20,
          humidity: 30,
          wind: 1.7,
        };
      },
    },
  },
};
</script>

<style scoped>
.weather-item {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border: 1px dotted #a8e063;
  padding: 1.2em;
}
.weather-item h3 {
  font-size: 20px;
  color: #333;
}
.temperature {
  font-size: 40px;
}
.info {
  font-size: 14px;
}
.rest {
  display: inline-block;
  width: 70px;
  justify-content: center;
  align-items: space-between;
  font-size: 12px;
  padding: 7px;
}
.weather-item * {
  line-height: 2;
}
</style>
