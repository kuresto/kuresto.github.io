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
          Existe um mito que a tecnologia é para ser utilizada não entendida. Utilizamos várias todos os dias sem
          entender o porque existem. O porque de certas decisões passam despercebido. Falamos em ambiente de trabalho
          de visão holística, mas não entendemos como criar esta visão.
        </p>

        <p>
          Antes de tudo para que se haja esta "visão" devemos empoderar o cliente e o usuário, e para empodera-lo
          temos que simplificar nossos pensamentos viciados em pensar como um computador responderá aos nossos comandos,
          e passar a pensar como nós pessoas entedemos a natureza e como isso influenciou a criação desta máquina.
        </p>

        <p>
          Meu foco como <strong>desenvolvedor</strong> é exatamente este! Não existe tecnologia sem
          <strong>descoberta</strong> e ela não continua existindo sem <strong>entendimento</strong>. Conhecimento
          deve ser compartilhado e ensinado, facilitando nosso trabalho e tornando nosso futuro um pouco menos escuro.
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
