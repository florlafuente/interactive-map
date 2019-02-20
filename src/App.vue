<template>
  <div id="app">
    <Nav :activeTopic="activeTopic" :changeTopic="changeTopic"/>
    <Map :activeTopic="activeTopic" />
  </div>
</template>

<script>
import Nav from './components/Nav.vue'
import Map from './components/Map.vue'

export default {
  name: 'app',
  components: {
    Nav,
    Map
  },
  data() {
    return {
      activeTopic: 'cupo-trans'
    }
  },
  methods: {
    changeTopic: function(newTopic) {
      this.activeTopic = newTopic
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>