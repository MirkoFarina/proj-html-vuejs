<script>
import CardEvents from './CardEvents.vue';
export default {
    name: 'TemplateEvent',
    props: {
        dataCard: Array
    },
    components: {
        CardEvents
    }
}
</script>

<template>
<div class="title mb-5 text-center">
    <h6 class="mb-4 mt-5">
       GET IN CONTACT NOW
    </h6>
    <h2>
        upcoming  <span>events</span> 
    </h2>
</div>
<div class="container">
    <div class="row row-cols-1 row-cols-lg-2 mb-5">
        <CardEvents :cards="dataCard"/>
    </div>
</div>
<div class="text-center go-to position-relative">
    <span>
        Excited about our event? <a href="#"> View all events  <i class="fa-solid fa-arrow-right-long"></i></a>
    </span>
</div>

</template>



<style lang="scss" scoped>
@use '../scss/partials/variables' as *;

.go-to {
    span {
        color: lighten($primary-color, 20%);
        font-weight: 700;
        a {
            color: $secondary-color;
            padding-bottom: 5px;
            border-bottom: 1px solid lightgray;
            &:hover {
                color: $primary-color-over;
            }
        }
    }
}

</style>