<template>
  <!-- Portfolio Section
    ================================================== -->
  <section id="skills" v-if="skills !== undefined">

    <div class="row">

      <div class="twelve columns collapsed">

        <h1>Mas o que você sabe fazer?</h1>

        <!-- portfolio-wrapper -->
        <div id="portfolio-wrapper" class="bgrid-quarters s-bgrid-thirds cf">

          <div class="columns portfolio-item" v-for="skill in skills">
            <div class="item-wrap">

              <a class="askill" :title="skill.titulo">
                <img :alt="skill.titulo" :src="skill.imagem">
                <div class="overlay">
                  <div class="portfolio-item-meta">
                    <h5>{{ skill.titulo }}</h5>
                    <p>{{ skill.descricao_curta }}</p>
                  </div>
                </div>
                <div class="link-icon"><i class="icon-plus"></i></div>
              </a>

            </div>
            <br>
          </div> <!-- item end -->

        </div>

      </div>

    </div>

  </section>
</template>

<script>
import YAML from 'yamljs'

export default {
  name: 'skills',
  computed: {
    skills () {
      return YAML.load('/static/seed/skills.yml')
    }
  },
  mounted: function () {
  }
}
</script>

<style scoped>

</style>
