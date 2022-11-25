<script>
import dataCardDream from '../data/dataCardDream';
import JumbotronApp from './JumbotronApp.vue';
import TemplateBuildDream from './TemplateBuildDream.vue';
import accordion from '../data/dataAccordion';
import TemplateCareerPerspective from './TemplateCareerPerspective.vue';
import StaticsApp from './StaticsApp.vue';
  export default {
    name: 'MainApp',
    components: {
      JumbotronApp,
      TemplateBuildDream,
      TemplateCareerPerspective,
      StaticsApp
    },
    data(){
        return {
            dataCardDream,
            accordion
        }
    }
  }
</script>

<template>
    <main>
        <jumbotron-app class="mb-5" />
        
        <section id="build-dream">
            <TemplateBuildDream :data="dataCardDream" />
        </section>

        <section id="career-perspective">
            <TemplateCareerPerspective :dataAccordion="accordion"/>
        </section>

        <section id="statistics">
            <StaticsApp />
        </section>
    </main>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
section {
  margin-bottom: 100px;
}
</style>