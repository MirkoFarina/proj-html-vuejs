<script>
import AccordionApp from './AccordionApp.vue';
export default {
    name: 'TemplateCareerPerspective',
    components: {
        AccordionApp
    }
}
</script>

<template>
    <div class="container">
        <div class="row row-cols-1 row-cols-lg-2">
            <div class="col text-center left">
                <img class="over" src="../assets/img/about-us-03-image-01.png" alt="Construc stunning">
            </div>
            <div class="col">
                <div class="title mb-5">
                    <h6 class="mb-4">
                        DREAM WHIT <span>MAXCOACH</span>
                    </h6>
                    <h2>
                        Construct a  <span>stunning</span> carrer perspective
                    </h2>
                </div>
                <AccordionApp />
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
    .left {
        position: relative;
        z-index: 1;
        &::after {
            content: '';
            position: absolute;
            top: 50px;
            left: -50px;
            background-image: url('../assets/img/underlay-shape-lilla.svg');
            background-repeat: no-repeat;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
    }
</style>