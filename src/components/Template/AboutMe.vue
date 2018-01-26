<template>
  <!-- About Section
  ================================================== -->
  <section id="sobre-mim">

    <div class="row">

      <div class="three columns">

        <img class="profile-pic" src="../../assets/img/logo.gif" alt="Meu avatar! Feito por Fellipe da Silva (Twitter: @cueinn)" />

      </div>

      <div class="nine columns main-col">

        <h2>Mas, assim, quem é você?</h2>

        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem
          aperiam,
          eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim
          ipsam
          voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui
          ratione
          voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur,
          adipisci velit,
          sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.
          Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam.
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
            <h2>Quero rabiscar umas anotações!</h2>
            <p>
              <a href="#" class="button">
                <i class="fa fa-download"></i>Baixe meu currículo, então!
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
