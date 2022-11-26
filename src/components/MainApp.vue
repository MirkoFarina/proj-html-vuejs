<script>
import {dataCardDream, dataAccordion, dataStatics, dataCardCourses,dataEvents, dataCardsCoach} from '../data/allDataSection';
//JUMBO
import JumbotronApp from './JumbotronApp.vue';
// BUILD DREAM 
import TemplateBuildDream from './TemplateBuildDream.vue';
// CARRER PERSPECTIVE
import TemplateCareerPerspective from './TemplateCareerPerspective.vue';
// STATICS
import StaticsApp from './StaticsApp.vue';
// COURSES
import TemplateCourses from './TemplateCourses.vue';
// QUESTION
import QuestionLeft from './QuestionLeft.vue';
import QuestionRight from './QuestionRight.vue';
//EVENTS
import TemplateEvent from './TemplateEvent.vue';
// COACH
import TemplateCoach from './TemplateCoach.vue';

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
      TemplateEvent,
      TemplateCoach
    },
    data(){
        return {
            dataCardDream,
            dataAccordion,
            dataStatics,
            dataCardCourses,
            dataEvents,
            dataCardsCoach
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

        <section id="coach">
            <TemplateCoach :dataCards="dataCardsCoach"/>
        </section>
    </main>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
section {
  margin-bottom: 100px;
}

#coach {
    background-color: #F8F8F8;
}
</style>