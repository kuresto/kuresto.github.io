<template>

  <!-- Resume Section
  ================================================== -->
  <section id="projetos">

    <!-- Education
    ----------------------------------------------- -->
    <div class="row education" v-if="philosofy.conteudo.length !== undefined">

      <div class="three columns header-col">
        <h1><span>Filosofia</span></h1>
      </div>

      <div class="nine columns main-col">

        <div class="row item">

          <div class="twelve columns">

            <h3>{{ philosofy.quote }}</h3>
            <p class="info">{{ philosofy.origin }}</p>

            <p>
              {{ philosofy.conteudo }}
            </p>

          </div>

        </div> <!-- item end -->

      </div> <!-- main-col end -->

    </div> <!-- End Education -->

    <!-- Work
    ----------------------------------------------- -->
    <div class="row work" v-if="featured.descricao !== undefined">

      <div class="three columns header-col">
        <h1><span>Projeto em destaque</span></h1>
      </div>

      <div class="nine columns main-col">

        <div class="row item">

          <div class="twelve columns">

            <h3>{{ featured.nome }}</h3>
            <p class="info">{{ featured.funcao }} <span>&bull;</span> <em class="date">{{ featured.ano }}</em></p>

            <p>
              {{ featured.descricao }}
            </p>

          </div>

        </div> <!-- item end -->

      </div> <!-- main-col end -->

    </div> <!-- End Work -->

    <!-- Skills
    ----------------------------------------------- -->
    <div class="row skill" v-if="projects.length !== 0">

      <div class="three columns header-col">
        <h1><span>Histórico</span></h1>
      </div>

      <div class="nine columns main-col">

        <div class="row item" v-bind="projects" v-for="project in projects">

          <div class="twelve columns">

            <h3>{{ project.nome }}</h3>
            <p class="info">{{ project.funcao }} <span>&bull;</span> <em class="date">{{ project.ano }}</em></p>

            <p>
              {{ project.descricao }}
            </p>

          </div>

        </div> <!-- item end -->

      </div> <!-- main-col end -->

    </div> <!-- End skills -->

  </section> <!-- Resume Section End-->

</template>

<script>
import YAML from 'yamljs'

export default {
  name: 'projects',
  computed: {
    featured () {
      return YAML.load('/static/seed/projetodestaque.yml')
    },
    projects () {
      return YAML.load('/static/seed/historico.yml')
    },
    philosofy () {
      return YAML.load('/static/seed/filosofia.yml')
    }
  }

}
</script>

<style scoped>

</style>
