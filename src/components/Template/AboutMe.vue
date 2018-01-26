<template>
  <!-- About Section
  ================================================== -->
  <section id="sobre-mim">

    <div class="row">

      <div class="three columns">

        <img class="profile-pic" src="../../assets/img/logo.gif"
             alt="Meu avatar! Feito por Fellipe da Silva (Twitter: @cueinn)"/>

      </div>

      <div class="nine columns main-col">

        <h2>Mas, assim, quem é você?</h2>

        <blockquote>
          Damn kid. Tying up the phone line again. They're all alike... <br>
          <small>Phrack Magazine, Vol 1, Issue 7, Phile 3 of 10 - Hacker Manifesto</small>
        </blockquote>

        <p>
          Começou com um terminal em BASIC. Eu tinha (tenho) um computador/vídeo game chamado Magic
          Computer, mas aquele um terminal roxo era que fazia coisas
          que eu não entendia. Fascinado, lembro de ter lido no manual (que acho que não era do aparelho)
          um programa que escrevia uma frase em inglês infinitas vezes: Hello world!
        </p>

        <p>
          Somente 15 anos depois aprendi a cancelar a execução do mesmo.
        </p>

        <p>
          Mas somente comecei a me interessar pela área de verdade mais tarde. Lembro dos choques que tomei com meu
          computador, tentativas de criar sites no Geocities da Yahoo!, caminhar pelo MSN Groups, não entender o que
          o Front Page tava fazendo, procurando como programar. E, lógico, o mais importante para mim era hackear meus
          jogos! O que começou como uma trapaça, virou um hobbie, e anos depois este hobbie virou filosofia.
        </p>

        <div class="row">

          <div class="columns contact-details">

            <h2>E como falo contigo?</h2>
            <p class="address">
              <span>Nilton Frederico Teixeira</span><br>
              <span>Ribeirão Preto/São Paulo</span><br>
              <span>
                <a href="mailto:niltonfrederico@gmail.com" title="Me envie um e-mail!" target="_blank">niltonfrederico@gmail.com</a>
              </span>
            </p>

          </div>

          <div class="columns download">
            <h2>Posso fazer umas anotações?</h2>
            <p>
              <a href="#" class="button">
                <i class="fa fa-download"></i>Claro! Baixe meu CV
              </a>
            </p>
          </div>

        </div> <!-- end row -->

      </div> <!-- end .main-col -->

    </div>

  </section> <!-- About Section End-->

</template>

<script>
export default {
  name: 'aboutMe'
}
</script>

<style scoped>
  .download h2 {
    margin-top: -6px
  }
</style>
