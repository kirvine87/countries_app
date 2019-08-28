<template lang="html">
  <div class="">
    <h2>{{country.name}}</h2>
    <p>Capital: {{country.capital}}</p>
    <p>Population: {{country.population}}</p>
  </div>
</template>

<script>
export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
</style>
