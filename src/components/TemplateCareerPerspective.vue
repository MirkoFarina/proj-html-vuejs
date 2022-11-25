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
            <div class="col text-center">
                <img src="../assets/img/about-us-03-image-01.png" alt="Construc stunning">
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

</style>