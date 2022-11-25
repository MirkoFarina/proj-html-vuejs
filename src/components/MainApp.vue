<script>
import dataCardDream from '../data/dataCardDream';
import JumbotronApp from './JumbotronApp.vue';
import TemplateBuildDream from './TemplateBuildDream.vue';
import accordion from '../data/dataAccordion';
import TemplateCareerPerspective from './TemplateCareerPerspective.vue';
import dataStatics from '../data/dataStatics';
import StaticsApp from './StaticsApp.vue';
import dataCardCourses from '../data/dataCardCourses';
import TemplateCourses from './TemplateCourses.vue';
import QuestionLeft from './QuestionLeft.vue';
import QuestionRight from './QuestionRight.vue'
  export default {
    name: 'MainApp',
    components: {
      JumbotronApp,
      TemplateBuildDream,
      TemplateCareerPerspective,
      StaticsApp,
      TemplateCourses,
      QuestionLeft,
      QuestionRight
    },
    data(){
        return {
            dataCardDream,
            accordion,
            dataStatics,
            dataCardCourses
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
            <StaticsApp :statics="dataStatics" />
        </section>

        <section id="courses">
            <TemplateCourses :dataCourses="dataCardCourses"/>
        </section>

        <section id="questions">
            <QuestionLeft/>
            <QuestionRight />
        </section>
    </main>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
section {
  margin-bottom: 100px;
}
</style>