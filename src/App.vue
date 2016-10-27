<template>
  <div id="app">
    <hello v-show="toggleHelloComponent"></hello>
    <RandomGallery v-show="toggleRandomGalleryComponent"></RandomGallery>
  </div>
</template>

<script>
import Hello from './components/Hello'
import RandomGallery from './components/RandomGallery'

export default {
  name: 'app',
  components: {
    Hello,
    RandomGallery
  },
  data () {
    return {
      toggleHelloComponent: true,
      toggleRandomGalleryComponent: false
    }
  },
  methods: {
    openRandomGalleryScreen () {
      this.toggleHelloComponent = false
      this.toggleRandomGalleryComponent = true
    }
  },
  mounted () {
    this.$on('openRandomGalleryScreen', this.openRandomGalleryScreen)
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
