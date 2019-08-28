<template lang="html">
  <div class="">
    <h2>{{country.name}}</h2>
    <p>Capital: {{country.capital}}</p>
    <p>Population: {{country.population}}</p>
    <h3>Languages:</h3>
    <p v-for="language of countriesLanguages"> {{language}}</p>
    <img :src="country.flag"></img>
  </div>
</template>

<script>
export default {
  name: 'country-detail',
  props: ['country'],
  computed: {
    countriesLanguages() {
      return this.country.languages.map((language) => {
        return language.name
      })
    }
  }
}
</script>

<style lang="css" scoped>
  img {
    width: 100px;
    height: 100px;
  }
</style>
