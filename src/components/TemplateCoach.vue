<script>
import SliderCoach from './SliderCoach.vue';
export default {
    name: 'TemplateCoach',
    components: {
        SliderCoach
    },
    props: {
        dataCards: Array
    }
}
</script>

<template>
    <div class="container">
        <div class="title mb-5 text-center">
            <h6 class="mb-4 mt-5">
               people are praising maxcoach
            </h6>
            <h2>
                what make they  <span>love us?</span> 
            </h2>
        </div>
        <SliderCoach :arrayCards="dataCards" />
    </div>
</template>

<style lang="scss" scoped>
.container {
    padding-top: 50px;
}
</style>