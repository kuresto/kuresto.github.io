<template>
  <main>

    <vue-header></vue-header>
    <about-me></about-me>
    <projects></projects>

  </main>
</template>

<script>
import Header from './Template/Header'
import AboutMe from './Template/AboutMe'
import Projects from './Template/Projects'

export default {
  name: 'Main',
  components: {
    'vue-header': Header,
    AboutMe,
    Projects
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
