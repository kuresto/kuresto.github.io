<template>
  <nav id="nav-wrap">

    <a class="mobile-btn" href="#nav-wrap" title="Show navigation">Show navigation</a>
    <a class="mobile-btn" href="#" title="Hide navigation">Hide navigation</a>

    <ul id="nav" class="nav">
      <li class="current"><a class="smoothscroll" href="#home">Contate-me</a></li>
      <li><a class="smoothscroll" href="#sobre-mim">Sobre mim</a></li>
      <li><a class="smoothscroll" href="#projetos">Projetos</a></li>
      <li><a class="smoothscroll" href="#skills">Habilidades</a></li>
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

      if ((y > h * 1) && (y < h) && (window.outerWidth > 768)) {

      } else {
        if (y < h * 1) {
          nav.classList.remove('opaque')
        } else {
          nav.className += ' opaque'
        }
      }
    }, false)

    // menu highlight
    let sections = {

    }
  }
}
</script>

<style scoped>

</style>
