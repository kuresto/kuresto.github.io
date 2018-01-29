<template>
  <nav id="nav-wrap">

    <a class="mobile-btn" href="#nav-wrap" title="Show navigation">Show navigation</a>
    <a class="mobile-btn" href="#" title="Hide navigation">Hide navigation</a>

    <ul id="nav" class="nav">
      <li class="current"><a class="smoothscroll" href="#inicio">Inicio</a></li>
      <li><a class="smoothscroll" href="#sobre-mim">Sobre mim</a></li>
      <li><a class="smoothscroll" href="#curriculo">Currículo</a></li>
      <li><a class="smoothscroll" href="#projetos">Projetos</a></li>
      <li><a class="smoothscroll" href="#depoimentos">Depoimentos</a></li>
      <li><a class="smoothscroll" href="#contate-me">Contate-me</a></li>
    </ul> <!-- end #nav -->

  </nav> <!-- end #nav-wrap -->
</template>

<script>
export default {
  name: 'top-menu',
  mounted: function () {
    // smoothscrooling
    let smoothscroll = document.getElementsByClassName('smoothscrool')

    smoothscroll.addEventListener('click', function (event) {
      event.preventDefault()

      let target = this.hash

      console.log(target)
    }, false)

    /* $('.smoothscroll').on('click', function (e) {
      e.preventDefault()

      var target = this.hash,
        $target = $(target)

      $('html, body').stop().animate({
        'scrollTop': $target.offset().top
      }, 800, 'swing', function () {
        window.location.hash = target
      })
    }) */
    // fade menu

    // menu highlight
  }
}
</script>

<style scoped>

</style>
