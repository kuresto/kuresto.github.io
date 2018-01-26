<template>
  <main>

    <vue-header></vue-header>

  </main>
</template>

<script>
import Header from './Template/Header'

export default {
  name: 'Main',
  components: { 'vue-header': Header },
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
