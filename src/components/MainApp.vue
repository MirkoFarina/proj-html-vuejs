<script>
import dataCardDream from '../data/dataCardDream';
import JumbotronApp from './JumbotronApp.vue';
import TemplateBuildDream from './TemplateBuildDream.vue';
import TemplateCareerPerspective from './TemplateCareerPerspective.vue';
  export default {
    name: 'MainApp',
    components: {
      JumbotronApp,
      TemplateBuildDream,
      TemplateCareerPerspective
    },
    data(){
        return {
            dataCardDream
        }
    }
  }
</script>

<template>
    <main>
        <jumbotron-app class="mb-5" />
        <section id="build-dream" class="mb-5">
            <TemplateBuildDream :data="dataCardDream" />
        </section>
        <section id="career-perspective">
            <TemplateCareerPerspective />
        </section>
    </main>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
</style>