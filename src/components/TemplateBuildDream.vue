<script>
import CardSectionDream from './CardSectionDream.vue';
export default {
    name:'TemplateBuildDream',
    props: {
        data: Array
    },
    components: {
        CardSectionDream
    }
}
</script>

<template>
    <div class="container">
        <div class="title text-center mb-5">
            <h6 class="mb-4">
                START LEARNING CODING LENGUAGES
            </h6>
            <h2>
                Build Your dream <span>TODAY</span>
            </h2>
        </div>
        <div class="row row-cols-2 row-cols-lg-4">
            <CardSectionDream v-for="(card, index) in data" 
                :key="index" 
                :card="card"/>  
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>