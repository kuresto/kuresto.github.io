<template>
  <main>

    <vue-header></vue-header>
    <about-me></about-me>
    <projects></projects>
    <the-footer></the-footer>

  </main>
</template>

<script>
import Header from './Template/Header'
import AboutMe from './Template/AboutMe'
import Projects from './Template/Projects'
import TheFooter from './Template/TheFooter'

export default {
  name: 'Main',
  components: {
    'vue-header': Header,
    AboutMe,
    Projects,
    TheFooter
  },
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
