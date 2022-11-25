<script>
import {dataCardDream, dataAccordion, dataStatics, dataCardCourses,dataEvents} from '../data/allDataSection';

import JumbotronApp from './JumbotronApp.vue';
import TemplateBuildDream from './TemplateBuildDream.vue';
import TemplateCareerPerspective from './TemplateCareerPerspective.vue';
import StaticsApp from './StaticsApp.vue';
import TemplateCourses from './TemplateCourses.vue';
import QuestionLeft from './QuestionLeft.vue';
import QuestionRight from './QuestionRight.vue';
import TemplateEvent from './TemplateEvent.vue';

  export default {
    name: 'MainApp',
    components: {
      JumbotronApp,
      TemplateBuildDream,
      TemplateCareerPerspective,
      StaticsApp,
      TemplateCourses,
      QuestionLeft,
      QuestionRight,
      TemplateEvent
    },
    data(){
        return {
            dataCardDream,
            dataAccordion,
            dataStatics,
            dataCardCourses,
            dataEvents
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
            <TemplateCareerPerspective :dataAccordion="dataAccordion"/>
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

        <section id="events">
            <TemplateEvent :dataCard="dataEvents" />
        </section>
    </main>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
section {
  margin-bottom: 100px;
}
</style>