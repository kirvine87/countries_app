<template lang="html">

  <select v-model="country" @change="onSelect">
    <option selected disabled value="">Select A Country</option>
    <option v-for="(country, index) of countries" :value="country" :key="index">{{country.name}}</option>
  </select>

</template>

<script>
import {eventBus} from '../main.js'

export default {
  name: 'country-select',
  data() {
    return {
      country: null
    }
  },
  props: ['countries'],
  methods: {
    onSelect(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
