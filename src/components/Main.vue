<template>
  <main>

    <vue-header></vue-header>
    <about-me></about-me>

  </main>
</template>

<script>
import Header from './Template/Header'
import AboutMe from './Template/AboutMe'

export default {
  name: 'Main',
  components: {
    'vue-header': Header,
    AboutMe
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
