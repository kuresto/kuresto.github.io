<template>
  <!-- Header ================================================== -->
  <header id="home">

    <top-menu></top-menu>

    <div class="row banner">
      <div class="banner-text">
        <h1 class="responsive-headline">
          <span>Olá! Eu sou</span> <br>
          Nilton Teixeira.
        </h1>
        <h3>Eu sou um <span>desenvolvedor full-stack</span> estacionado em Ribeirão Preto/SP.
          Procuro <span>desenvolver para humanos</span> através do desapego a crenças engessadas, colocando
          <span>conceitos acima da ferramentas</span>. <br>
          Ficou curioso? <a class="smoothscroll" href="#sobre-mim">Me conheça melhor logo abaixo!</a>
        </h3>
        <hr/>
        <ul class="social">
          <li><a href="https://github.com/kuresto" title="Meu GitHub" target="_blank"><i class="fa fa-github"></i></a>
          </li>
          <li><a href="https://www.linkedin.com/in/nilton-teixeira-22069a106" target="_blank" title="Meu LinkedIn">
            <i class="fa fa-linkedin"></i>
          </a></li>
          <li><a href="https://twitter.com/whoiskuresto" target="_blank" title="Meu Twitter"><i
            class="fa fa-twitter"></i></a></li>
          <li><a href="https://www.facebook.com/kuresto"><i class="fa fa-facebook"></i></a></li>
          <li><a href="mailto:niltonfrederico@gmail.com" title="Me envie um e-mail!" target="_blank"><i
            class="fa fa-envelope"></i></a></li>
        </ul>
      </div>
    </div>

    <p class="scrolldown">
      <a class="smoothscroll" href="#sobre-mim"><i class="fa fa-chevron-down"></i></a>
    </p>

  </header>
</template>

<script>
import TopMenu from './TopMenu'

export default {
  name: 'hero',
  components: {
    TopMenu
  },
  mounted () {
    const header = document.getElementsByTagName('header')[0]
    header.style.minHeight = getWindowHeight() + 'px'

    window.addEventListener('resize', function () {
      header.style.minHeight = getWindowHeight() + 'px'
    }, false)

    function getWindowHeight () {
      // make sure that window height is being correctly fetched
      let w = window
      let d = document
      let e = d.documentElement
      let g = d.getElementsByTagName('body')[0]

      return w.innerHeight || e.clientHeight || g.clientHeight
    }
  }
}

</script>

<style scoped>

</style>
