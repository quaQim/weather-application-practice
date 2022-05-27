<template>
  <div>
    <ul class="city-selector">
      <li
        @click="selectCity(city)"
        :class="{ isSelected: city.selected }"
        v-for="city in cities"
        :key="city.code"
      >
        {{ city.label }}
      </li>
    </ul>
    <link
      href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,800&display=swap"
      rel="stylesheet"
    />
  </div>
</template>

<script>
export default {
  name: "City-Selector",
  data() {
    return {
      cities: [
        { code: "seoul", label: "Seoul", selected: false },
        { code: "tokyo", label: "Tokyo", selected: false },
        { code: "paris", label: "Paris", selected: false },
        { code: "london", label: "London", selected: false },
        { code: "new york", label: "New york", selected: false },
        { code: "toronto", label: "Toronto", selected: false },
        { code: "milan", label: "Milan", selected: false },
        { code: "moscow", label: "Moscow", selected: false },
        { code: "beijing", label: "Beijing", selected: false },
        { code: "iksan", label: "Iksan", selected: false },
      ],
    };
  },
  methods: {
    selectCity(city) {
      city.selected = !city.selected;
      this.$emit("selectCity", city);
    },
  },
};
</script>

<style scoped>
.city-selector {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  color: #5b5f62;
}
.city-selector li {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid #c8c5ad;
  padding: 0.3em;
  cursor: pointer;
  font-family: "Playfair Display", serif;
}
.isSelected {
  background: #c1bc92;
  color: white;
  font-family: "Playfair Display", serif;
}
</style>
