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
            <p class="info">
              <small>{{ philosofy.origin }}</small>
            </p>

            <p v-html="philosofy.conteudo"></p>

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

            <h3>
              {{ featured.nome }}
              <small>
                <a :href="featured.url" target="_blank" :title="featured.nome">
                  <em class="fa fa-fw fa-external-link"></em>
                </a>
              </small>
            </h3>
            <p class="info">{{ featured.funcao }} <span>&bull;</span> <em class="date">{{ featured.ano }}</em></p>

            <p v-html="featured.descricao"></p>

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

            <h3>{{ project.nome }}
              <small v-if="project.url !== null">
                <a :href="project.url" target="_blank" :title="project.nome">
                  <em class="fa fa-fw fa-external-link"></em>
                </a>
              </small>
            </h3>
            <p class="info">{{ project.funcao }} <span>&bull;</span> <em class="date">{{ project.ano }}</em></p>

            <p v-html="project.descricao"></p>

            <ul>
              <li v-for="job in project.jobs">
                <a :href="job.url" target="_blank" :title="job.nome">{{ job.nome }}</a>
                <br>
                <small v-if="job.comment !== null">{{job.comment}}</small>
              </li>
            </ul>

            <p v-if="project.jobs !== undefined">Entre outros.</p>

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
