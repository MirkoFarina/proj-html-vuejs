<script>
import CardCoach from './CardCoach.vue'
import { Swiper, SwiperSlide} from 'swiper/vue';
import {Pagination } from 'swiper';
import 'swiper/css/bundle';
    export default {
        name: 'SliderCoach',
        components: {
            Swiper,
            SwiperSlide,
            CardCoach
        },
        props: {
            arrayCards: Array
        },
        setup () {
            return {
                modules: [Pagination]
            }
        }
    }
</script>
<template>
    <swiper
    :modules="modules"
    :slides-per-view="3"
    :space-between="50"
    :pagination="{ clickable: true }">
       <SwiperSlide v-for="(card, index) in arrayCards" :key="index" class="mb-5">
           <CardCoach :card="card"/>
       </SwiperSlide>
    </swiper>
</template>


<style lang="scss" >
@use '../scss/partials/variables' as *;
.swiper-pagination-bullet-active {
    background-color: $primary-color;
    width: 10px;
    height: 10px;
}
</style>