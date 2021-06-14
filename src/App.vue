<template>
  <h1 class="logo">
    <img src="./assets/logo.svg" alt="Pokedex" />
  </h1>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #ffd924;
}

.logo {
  margin: 30px auto 0 auto;
  text-align: center;
}

.logo img {
  max-width: 300px;
}
</style>
