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
    window.addEventListener('scroll', function () {
      let sections = {
        contato: {
          id: '#home',
          top: getY('#home').top,
          bottom: getY('#home').bottom
        },
        sobre: {
          id: '#sobre-mim',
          top: getY('#sobre-mim').top,
          bottom: getY('#sobre-mim').bottom
        },
        projetos: {
          id: '#projetos',
          top: getY('#projetos').top,
          bottom: getY('#projetos').bottom
        },
        habilidades: {
          id: '#skills',
          top: getY('#skills').top,
          bottom: getY('#skills').bottom
        }
      }

      let id = function () {
        let valids = []
        for (let section in sections) {
          if (sections[section].top >= 0) {
            valids.push(sections[section].id)
          }
        }

        return valids[0]
      }

      let elem = document.querySelector('a[href="' + id() + '"]')
      let elems = document.querySelector('nav li.current')

      if (elems !== null) {
        elems.classList.remove('current')
      }

      if (elem !== null) {
        elem.parentElement.className += ' current'
      }
    }, false)

    function getY (query) {
      let elem = document.querySelector(query)
      let rect = elem.getBoundingClientRect()

      return {
        top: rect.top,
        bottom: rect.bottom
      }
    }
  }
}
</script>

<style scoped>

</style>
