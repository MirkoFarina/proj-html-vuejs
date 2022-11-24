<script>
import JumbotronApp from './JumbotronApp.vue';
import CardSectionDream from './CardSectionDream.vue';
import dataCardDream from '../data/dataCardDream';
  export default {
    name: 'MainApp',
    components: {
      JumbotronApp,
      CardSectionDream
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
        <section id="build-dream">
            <div class="container">
                <div class="title text-center mb-5">
                    <h6>
                        START LEARNING CODING LENGUAGES
                    </h6>
                    <h2>
                        Build Your dream <span>TODAY</span>
                    </h2>
                </div>
                <div class="row row-cols-2 row-cols-lg-4">
                    <CardSectionDream v-for="(card, index) in dataCardDream" 
                    :key="index" 
                    :card="card"/>  
                </div>
            </div>
        </section>
    </main>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
    .title {
        h6 {
            color: $text-color;
        }
        h2 {
            color: $primary-color;
            text-transform: capitalize;
            font-size: 3rem;
            font-weight: 700;
        span {
            color: $secondary-color;
            font-weight: 400;
        }
        }
    }
</style>