<script>
import CardCourses from './CardCourses.vue';
export default {
    name:'TemplateCourses',
    props: {
        dataCourses: Array
    },
    components: {
        CardCourses
    }
}
</script>

<template>
    <div class="container">
        <div class="title text-center mb-5">
            <h6 class="mb-4">
               Choose where you'd like to begin
            </h6>
            <h2>
                latest featured <span>courses</span>
            </h2>
        </div>
        <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 mb-5">
            <CardCourses v-for="(card, index) in dataCourses" :key="index" :content="card" />
        </div>
        <div class="row">
            <div class="col-4 offset-4">
                <button type="button" class="btn mf-button  btn-lg">
                    View all courses 
                    <i class="fa-solid fa-arrow-right-long"></i>
                </button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/variables' as *;

    button {
        padding: 13px 50px;
    }
</style>