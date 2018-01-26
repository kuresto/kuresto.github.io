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
          Acredito em <span>desenvolver para humanos</span>, deixando de lado crenças engessadas e colocando
          <span>conceito sobre ferramenta</span>. <br>
          Ficou curioso? <a class="smoothscroll" href="#about">Me conheça melhor logo abaixo!</a>
        </h3>
        <hr/>
        <ul class="social">
          <li><a href="#"><i class="fa fa-github"></i></a></li>
          <li><a href="#"><i class="fa fa-linkedin"></i></a></li>
          <li><a href="#"><i class="fa fa-twitter"></i></a></li>
          <li><a href="#"><i class="fa fa-facebook"></i></a></li>
          <li><a href="#"><i class="fa fa-envelope"></i></a></li>
        </ul>
      </div>
    </div>

    <p class="scrolldown">
      <a class="smoothscroll" href="#about"><i class="icon-down-circle"></i></a>
    </p>

  </header>
</template>

<script>
import Menu from './Menu'

export default {
  name: 'hero',
  components: {
    'top-menu': Menu
  }
}
</script>

<style scoped>

</style>
