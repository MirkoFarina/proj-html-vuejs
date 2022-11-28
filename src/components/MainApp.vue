<script>
import {
  dataCardDream,
  dataAccordion,
  dataStatics,
  dataCardCourses,
  dataEvents,
  dataCardsCoach,
} from "../data/allDataSection";
//JUMBO
import JumbotronApp from "./JumbotronApp.vue";
// BUILD DREAM
import TemplateBuildDream from "./TemplateBuildDream.vue";
// CARRER PERSPECTIVE
import TemplateCareerPerspective from "./TemplateCareerPerspective.vue";
// STATICS
import StaticsApp from "./StaticsApp.vue";
// COURSES
import TemplateCourses from "./TemplateCourses.vue";
// QUESTION
import QuestionLeft from "./QuestionLeft.vue";
import QuestionRight from "./QuestionRight.vue";
//EVENTS
import TemplateEvent from "./TemplateEvent.vue";
// COACH
import TemplateCoach from "./TemplateCoach.vue";

export default {
  name: "MainApp",
  components: {
    JumbotronApp,
    TemplateBuildDream,
    TemplateCareerPerspective,
    StaticsApp,
    TemplateCourses,
    QuestionLeft,
    QuestionRight,
    TemplateEvent,
    TemplateCoach,
  },
  data() {
    return {
      dataCardDream,
      dataAccordion,
      dataStatics,
      dataCardCourses,
      dataEvents,
      dataCardsCoach,
    };
  },
};
</script>

<template>
  <main>
    <jumbotron-app class="mb-5" />

    <section id="build-dream">
      <TemplateBuildDream :data="dataCardDream" />
    </section>

    <section id="career-perspective">
      <TemplateCareerPerspective :dataAccordion="dataAccordion" />
    </section>

    <section id="statistics">
      <StaticsApp :statics="dataStatics" />
    </section>

    <section id="courses">
      <TemplateCourses :dataCourses="dataCardCourses" />
    </section>

    <!-- WAVE -->
    <div class="position-relative">
      <div class="bg-image rounded-7 shadow-5">
        <svg
          data-name="Layer 1"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 1200 120"
          preserveAspectRatio="none"
          style="
            opacity: 1;
            width: 260%;
            height: 130px;
            fill: #f6f6f6;
            transform: rotateY(0deg);
          "
        >
          <path
            d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"
          ></path>
        </svg>
      </div>
    </div>
    <!-- /WAVE -->

    <section id="questions">
      <QuestionLeft />
      <QuestionRight />
    </section>

    <section id="events">
      <TemplateEvent :dataCard="dataEvents" />
    </section>

    <section id="coach">
      <TemplateCoach :dataCards="dataCardsCoach" />
    </section>
  </main>
</template>


<style lang="scss" scoped>
@use "../scss/partials/variables" as *;
section {
  margin-bottom: 100px;
}

#courses {
  background-image: linear-gradient(180deg, white, #f6f6f6);
  margin-bottom: 0;
  padding-bottom: 80px;
}

#coach {
  background-color: #f6f6f6;
  position: relative;
}
</style>