<template lang="html">

  <input @change="onInput" type="text" v-model="countryName">

</template>

<script>
import {eventBus} from '../main.js'

export default {
  name: 'country-search',
  props: ['countries'],
  data(){
    return {
      countryName: ""
    }
  },
  methods: {
    onInput() {
      for (let country of this.countries) {
        if (this.countryName === country.name) {
          return eventBus.$emit('country-selected', country)
        };
      }
    }
  }

}
</script>

<style lang="css" scoped>
input {
  width: 150px;
  height:25px;
}
</style>
