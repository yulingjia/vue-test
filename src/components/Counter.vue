<template>
  <div class="Counter">
    Counter is:{{ count }} <br /><br />
    <button type="button" @click="increment">+5</button>
    <button type="button" @click="decrement">-3</button>
  </div>
</template>

<script>
import {mapGetters, mapActions} from 'vuex'
export default {
  computed: {
    ...mapGetters(['count'])
  },
  methods: mapActions([
    'increment',
    'decrement'
  ])
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
