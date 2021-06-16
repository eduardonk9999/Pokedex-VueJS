<template>
  <h1 class="logo">
    <img src="./assets/logo.svg" alt="Pokedex" />
  </h1>

  <div class="wrapper">
    <input
      type="text"
      class="pesquisaPokemon"
      placeholder="Busque seu Pokémon"
    />

    <article class="pokes">
      <div class="wrapper">
        <ul class="lsitPokemons">
          <li v-for="(poke, index) in pokeList" :key="index">
            {{ poke.name }}
          </li>
        </ul>
      </div>
    </article>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pokeList: [
        {
          name: "Poke",
        },
        {
          name: "Poke2",
        },
      ],
    };
  },
  created() {
    fetch("https://pokeapi.co/api/v2/pokemon/")
      .then((response) => response.json())
      .then((data) => console.log(data));
  },
  methods: {},
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

.wrapper {
  max-width: 1440px;
  width: 100%;
  margin: 0 auto;
}

.logo {
  margin: 30px auto 0 auto;
  text-align: center;
}

.logo img {
  max-width: 300px;
}

.pesquisaPokemon {
  display: block;
  max-width: 500px;
  width: 100%;
  margin: 30px auto 0 auto;
  height: 40px;
  padding: 10px 0px 7px 30px;
  border: none;
  border-radius: 70px;
  background: #ce1030;
  color: #fff;
}

.pesquisaPokemon::placeholder {
  color: #fff;
  font-size: 16px;
}
ul.lsitPokemons {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}

ul.lsitPokemons li {
  list-style: none;
  margin: 0 10px;
}
</style>
