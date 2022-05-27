<template>
  <header class="header">
    <h2>Weather Application</h2>
    <p>Hello!</p>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,800&display=swap"
      rel="stylesheet"
    />
  </header>
</template>

<script>
export default {
  name: " HeaderDispaly",
};
</script>

<style scoped>
.header {
  background: linear-gradient(90deg, #ada996, #dbdbdb);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 2em;
}
.header h2 {
  color: #232526;
  font-size: 35px;
  font-family: "Playfair Display", serif;
}
.header p {
  color: #414345;
  font-family: "Playfair Display", serif;
}
</style>
