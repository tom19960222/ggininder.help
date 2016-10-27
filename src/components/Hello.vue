<template>
  <div class="hello">
    <img src="../assets/logo.png">
    <h1>{{ msg }}</h1>
    <button @click="gotoMainScreen">{{ btnMsg }}</button>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to GGININDER.HELP',
      btnMsg: 'HELP MY GG'
    }
  },
  methods: {
    gotoMainScreen () {
      console.debug('Help my GG!')
      this.$parent.$emit('openRandomGalleryScreen', null)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

button {
  width: 250px;
  height: 75px;
  font-size: 30px;
}
</style>
