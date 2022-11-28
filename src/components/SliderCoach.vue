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
        data () {
      return { 
        // RESPONSIVE SWIPER ADD BREAK POINTS
        swiperOptions: {
          breakpoints: {
      320: {
         slidesPerView: 1,
         spaceBetween: 10
      },
      700: {
         slidesPerView: 2,
         spaceBetween: 50
      },
      992: {
         slidesPerView: 3,
         spaceBetween: 50
      } 
   }   
        }
      }
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
    :breakpoints="swiperOptions.breakpoints"
    :modules="modules"
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