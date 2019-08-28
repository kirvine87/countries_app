<!-- <template lang="html">
  <li @click="handleClick">{{country.name}}</li>
</template>

<script>
import {eventBus} from '../main.js'

export default {
  name: 'list-component',
  props: ['country'],
  methods: {
    handleClick(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>

<style lang="css" scoped>
li:hover {
  text-shadow: 0 0 3px lightseagreen;
  font-size: 1.25em;
}
</style> -->
