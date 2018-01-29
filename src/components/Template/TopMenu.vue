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
    let smoothscroll = document.getElementsByClassName('smoothscroll')

    if (smoothscroll.length > 0) {
      for (let i = 0; i < smoothscroll.length; i++) {
        let elem = smoothscroll[i]

        elem.addEventListener('click', function (event) {
          event.preventDefault()

          document.getElementById(this.hash.replace('#', '')).scrollIntoView({
            behavior: 'smooth'
          })
        }, false)
      }
    }

    // fade menu
    window.addEventListener('scroll', function () {
      let h, y, nav

      h = document.getElementsByTagName('header')[0].clientHeight
      y = document.documentElement.scrollTop
      nav = document.getElementById('nav-wrap')

      if ((y > h * 0.90) && (y < h) && (window.outerWidth > 768)) {
        nav.className += ' fadeOut animated'
        nav.classList.remove('fadeIn')
        nav.classList.remove('animated')
      } else {
        if (y < h * 0.90) {
          nav.classList.remove('opaque')
          nav.classList.remove('fadeOut')
          nav.classList.remove('animated')
          nav.className += ' fadeIn animated'
        } else {
          nav.className += ' opaque'
          nav.className += ' fadeIn animated'
          nav.classList.remove('fadeOut')
          nav.classList.remove('animated')
        }
      }
    }, false)
    // menu highlight
  }
}
</script>

<style scoped>

</style>
